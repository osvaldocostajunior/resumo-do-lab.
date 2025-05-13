# resumo-do-lab. 

   Ferramentas de Gerenciamento e Implantação no Azure
 Azure Resource Manager (ARM)
Função: Controla como os recursos do Azure são implantados, gerenciados e monitorados.

Modelo: Declarativo (via templates JSON).

Uso comum: Infraestrutura como código (IaC) com ARM templates.

 Bicep
Função: Linguagem para criar arquivos de implantação de forma mais simples.

Modelo: Declarativo.

Vantagens:

Mais legível que JSON.

Compila para ARM templates.

Foco exclusivo no Azure.

 Terraform
Função: Ferramenta de IaC para criar e gerenciar recursos.

Modelo: Declarativo (HCL).

Vantagens:

Multi-cloud (Azure, AWS, GCP).

Automatização e controle de estado.

 Azure CLI
Função: Ferramenta de linha de comando para gerenciar recursos do Azure.

Modelo: Imperativo (comandos diretos).

Uso comum: Scripts, automações rápidas, testes.

 Azure PowerShell
Função: Módulo PowerShell para administrar o Azure via comandos.

Modelo: Imperativo.

Ideal para: Administradores e DevOps.

 Azure Portal
Função: Interface gráfica (GUI) para criar, visualizar e gerenciar recursos do Azure.

Uso comum: Tarefas manuais e visuais, aprendizado.

 Azure DevOps / GitHub Actions
Função: Ferramentas de CI/CD para automação de builds, testes e implantações.

Integração: Permite implantar usando Bicep, ARM, Terraform, etc.

📋 Resumo Final
Ferramenta	Tipo	Modelo	Foco
ARM Templates	Implantação	Declarativo	Infraestrutura (JSON)
Bicep	Implantação	Declarativo	Azure (moderno)
Terraform	Implantação	Declarativo	Multi-cloud
Azure CLI	Gerenciamento	Imperativo	Scripts e automação
Azure PowerShell	Gerenciamento	Imperativo	Scripts (Windows)
Azure Portal	Gerenciamento	Visual	Interface web
Azure DevOps / GitHub	Implantação	Automatizado	CI/CD
