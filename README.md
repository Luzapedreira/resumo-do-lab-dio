# resumo-do-lab-dio
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do curso Microsoft Azure Essentials na DIO.

## Microsoft Azure - Localizando Serviços por Categoria
Como criar conta no Miscrosoft Azure
Apresentação do portal e visualização de serviços disponíveis
Sobre base de rede também, como Bastions

## Criando Máquinas Virtuais na Azure
SLA - entender a implicação do tempo de uso ou de inatividade, no custo do serviço.
Quanto mais 9's menos tempo indisponível.
Ao criar máquina virtual, no portal podem ser escolhidas opções de indisponibilidade.

## Configurando uma instância de Banco de Dados na Azure
Tipos de serviços de Nuvem:
  -  Infraestrutura como Serviço (IaaS): Oferece recursos de infraestrutura, como servidores, armazenamento, e rede, de forma escalável e sob demanda.
  -  Plataforma como Serviço (PaaS): Oferece um ambiente de desenvolvimento e implementação, permitindo que desenvolvedores criem, testem e gerenciem aplicativos sem se preocupar com a       infraestrutura subjacente.
  -  Software como Serviço (SaaS): Fornece software pronto para uso, acessível pela internet, sem necessidade de instalação ou manutenção.

## Construindo Arquiteturas no Azure
1. Pares de Região (Region Pairs): Duas regiões do Azure emparelhadas geograficamente para garantir alta disponibilidade e recuperação de desastres.
Vantagens:
Replicação automática de dados entre regiões emparelhadas.
Failover prioritário: No caso de uma falha em uma região, a outra região do par pode ser ativada.
Atualizações escalonadas: As atualizações de infraestrutura são aplicadas em momentos diferentes para minimizar interrupções.
Exemplo: Brasil Sul e Sul dos EUA.
2. Grupos de Recursos (Resource Groups): Contêiner lógico que organiza e agrupa recursos como VMs, bancos de dados e redes que compartilham o mesmo ciclo de vida.
Vantagens:
Gerenciamento centralizado: Todos os recursos são tratados como uma unidade, facilitando a implantação e o monitoramento.
Controle de custo e uso: Cada grupo pode ter tags que ajudam a acompanhar os gastos e alocar custos.
Automação: Ferramentas como Azure Resource Manager (ARM) facilitam a implementação e atualização de recursos do grupo.
Exemplo de recursos em um grupo: VM + Storage + VNet associados a uma única aplicação.
3. Grupos de Gerenciamento (Management Groups): Estrutura hierárquica para organizar várias assinaturas do Azure, facilitando a governança em larga escala.
Vantagens:
Aplicação de políticas e controle de acesso: Definição de regras de segurança e compliance por grupo.
Herança automática: As políticas aplicadas a um grupo de gerenciamento são herdadas por todas as assinaturas e recursos abaixo dele.
Melhor governança: Útil para organizações que gerenciam múltiplas assinaturas e precisam aplicar controles consistentes.
Exemplo: Uma organização com várias unidades de negócios pode ter um grupo para cada unidade, como TI, RH e Finanças.
Esses componentes ajudam a garantir alta disponibilidade, organização eficiente e governança robusta no uso dos recursos do Azure, facilitando a escalabilidade e controle da infraestrutura em ambientes corporativos complexos.

