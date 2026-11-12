#!/bin/bash

# Encerra o script imediatamente se algum comando falhar
set -e

echo "=== Iniciando o provisionamento do Servidor Web ==="

# 1. Verifica se o script está sendo executado como root
if [ "$EUID" -ne 0 ]; then
  echo "Erro: Execute este script como root ou usando sudo."
  exit 1
fi

# 2. Atualiza a lista de pacotes do sistema
echo "[1/5] Atualizando repositórios do Ubuntu..."
apt-get update -y

# 3. Instala o servidor web Apache2
echo "[2/5] Instalando o Apache2..."
DEBIAN_FRONTEND=noninteractive apt-get install -y apache2

# 4. Inicia o serviço e habilita no boot do sistema
echo "[3/5] Habilitando e iniciando o serviço Apache2..."
systemctl enable apache2
systemctl start apache2

# 5. Configura o firewall UFW (caso esteja ativo) para liberar HTTP e HTTPS
echo "[4/5] Configurando regras de firewall..."
if command -v ufw > /dev/null; then
    ufw allow 'Apache Full'
    echo "Porta 80 (HTTP) e 443 (HTTPS) liberadas no UFW."
fi

# 6. Cria uma página HTML customizada de validação
echo "[5/5] Criando página web inicial..."
cat << 'EOF' > /var/www/html/index.html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Servidor Web Provisionado</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 80px; background-color: #f4f4f9; color: #333; }
        .card { background: white; padding: 30px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); display: inline-block; }
        h1 { color: #2e7d32; }
    </style>
</head>
<body>
    <div class="card">
        <h1>Servidor Web Ativo!</h1>
        <p>Este servidor foi provisionado automaticamente via script Bash.</p>
        <p>Protocolo HTTP operando na porta 80.</p>
    </div>
</body>
</html>
EOF

# Ajusta as permissões padrão do diretório web
chown -R www-data:www-data /var/www/html
chmod -R 755 /var/www/html

# Exibe o IP da máquina para acesso imediato
IP_SERVIDOR=$(hostname -I | awk '{print $1}')
echo "==================================================="
echo "Provisionamento concluído com sucesso!"
echo "Acesse no navegador: http://${IP_SERVIDOR}"
echo "==================================================="
