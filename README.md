# resumo-do-lab. 
Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

estou gostando estou utilizando direto no portal do aluno efetuando a criação de maquina  instancia 
estou aprendendo muito 
montei um laboratorio bem legal pra usar em casa como ja trabalho estou mesmo so me atualizando mais estou adorando o curso  




1. AzCopy
O AzCopy é uma ferramenta de linha de comando usada para transferir dados de e para o Azure Storage de maneira eficiente. Ele permite copiar blobs, arquivos e outros tipos de armazenamento no Azure, suportando transferências assíncronas e multithreading para melhorar a velocidade.

✅ Principais características:

Copia dados entre contas de armazenamento do Azure.

Suporta transferência de blobs, arquivos e tabelas.

Pode ser usado para sincronizar arquivos locais com o Azure Storage.

Permite transferências de dados para e de serviços como Azure Blob Storage, Azure Files e Amazon S3.

2. Contas de Armazenamento do Azure
Uma conta de armazenamento do Azure é um contêiner que armazena objetos de dados no Azure, incluindo blobs, filas, tabelas e arquivos.

✅ Requisitos importantes:

O nome deve ser globalmente único dentro do Azure.

Deve seguir restrições de nomenclatura (somente letras minúsculas e números).

Pode ser criada em qualquer Resource Group dentro de uma assinatura do Azure.

Pode ser gerenciada via Portal do Azure, CLI, PowerShell, SDKs ou ARM Templates.

3. Azure Data Box
O Azure Data Box é um serviço para mover grandes volumes de dados para o Azure usando dispositivos físicos fornecidos pela Microsoft. É ideal para cenários onde a transferência via internet não é prática devido ao tempo ou custo da largura de banda.

✅ Principais características:

Suporta a transferência de até 1 PB de dados por envio.

Os dispositivos são enviados ao cliente, que copia os dados localmente e os envia de volta para a Microsoft para upload no Azure.

Oferece opções como Data Box Disk, Data Box e Data Box Heavy, dependendo da quantidade de dados.

4. Arquivos do Azure (Azure Files)
O Azure Files é um serviço de armazenamento de arquivos em nuvem totalmente gerenciado, acessível via o protocolo SMB (Server Message Block). Ele permite que múltiplas VMs e serviços acessem os mesmos arquivos como se estivessem em um compartilhamento de rede tradicional.

✅ Principais características:

Suporte a SMB e NFS para compartilhamento de arquivos.

Possui replicação de dados para alta disponibilidade.

Permite integração com Active Directory (AD) para controle de permissões.

Pode ser montado em máquinas Windows, Linux e Mac.

5. ExpressRoute
O Azure ExpressRoute é um serviço que permite conexões privadas e dedicadas entre data centers locais e o Azure, proporcionando maior velocidade, segurança e confiabilidade em comparação com conexões de internet pública.

✅ Principais características:

Baixa latência e maior largura de banda para acessar serviços do Azure.

Conexões privadas diretas com Microsoft 365, Dynamics 365 e Azure.

Disponível em diferentes velocidades, de 50 Mbps a 100 Gbps.

Pode ser combinado com VPNs para soluções híbridas.
