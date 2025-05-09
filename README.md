# resumo-do-lab. 

   O Gerenciamento de Custos do Microsoft Azure (Azure Cost Management)
 é um conjunto de ferramentas e recursos que ajuda você a monitorar, alocar, otimizar e controlar os gastos na nuvem. Ele é essencial para garantir que os recursos do Azure sejam usados de forma eficiente e dentro do orçamento.


Monitorar gastos em tempo real

Definir orçamentos e alertas

Análise detalhada dos custos

O Gerenciamento de Custos do Azure também cobre recursos do Azure e do AWS, caso você esteja usando ambos por meio do Azure Cost Management + Billing (em parceria com o Cloudyn).


1. Marcas do Azure (Azure Tags)
Usadas para organizar logicamente os recursos.

Funcionam com pares chave-valor.

Facilitam a gestão, automação e relatórios (como por departamento ou ambiente).

✅ 2. Bloqueios de Recursos do Azure (Azure Resource Locks)
Evitam exclusão ou alterações acidentais em recursos importantes.

Dois tipos:

CanNotDelete: impede a exclusão.

ReadOnly: impede qualquer modificação.

3. Azure Policy
Permite criar regras e controles para garantir conformidade.

Aplicada a recursos, grupos de recursos ou assinaturas.

Exemplo: impedir criação de VMs em regiões não autorizadas, exigir tags, etc.
 4. Microsoft Purview
Solução para governança, risco e conformidade de dados.

Oferece uma visão unificada de dados em nuvem e local.

Ajuda no cumprimento de regulamentações como LGPD/GDPR.

O que não se aplica nesses casos:
MFA (Autenticação Multifator): é uma medida de segurança de login, não de governança.

Política simétrica/assimétrica: termos relacionados à criptografia, não à gestão de recursos no Azure.

Classificação de segurança: mostra o nível de segurança, mas não define regras como o Azure Policy.
