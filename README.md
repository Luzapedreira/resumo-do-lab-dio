## resumo-do-lab-dio
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do curso Microsoft Azure Essentials na DIO.

### Microsoft Azure - Localizando Serviços por Categoria
Como criar conta no Miscrosoft Azure
Apresentação do portal e visualização de serviços disponíveis
Sobre base de rede também, como Bastions

### Criando Máquinas Virtuais na Azure
SLA - entender a implicação do tempo de uso ou de inatividade, no custo do serviço.
Quanto mais 9's menos tempo indisponível.
Ao criar máquina virtual, no portal podem ser escolhidas opções de indisponibilidade.

### Configurando uma instância de Banco de Dados na Azure
Tipos de serviços de Nuvem:
  -  Infraestrutura como Serviço (IaaS): Oferece recursos de infraestrutura, como servidores, armazenamento, e rede, de forma escalável e sob demanda.
  -  Plataforma como Serviço (PaaS): Oferece um ambiente de desenvolvimento e implementação, permitindo que desenvolvedores criem, testem e gerenciem aplicativos sem se preocupar com a       infraestrutura subjacente.
  -  Software como Serviço (SaaS): Fornece software pronto para uso, acessível pela internet, sem necessidade de instalação ou manutenção.

### Construindo Arquiteturas no Azure
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

### Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure
Computação no Azure
- Azure Virtual Machines (VMs): Máquinas virtuais configuráveis para rodar sistemas operacionais e aplicativos.
  
- Azure App Service: Hospeda aplicativos web e APIs sem precisar gerenciar a infraestrutura.
  
- Azure Functions: Computação serverless para executar código sob demanda com base em eventos.
  
- Azure Kubernetes Service (AKS): Gerencia e orquestra contêineres em escala.
  
- Azure Batch: Automatiza o processamento de grandes volumes de trabalho em paralelo.

Serviços de Rede no Azure
- Azure Virtual Network (VNet): Criação de redes privadas na nuvem para conectar recursos.

- Azure Load Balancer: Distribui o tráfego para manter alta disponibilidade entre instâncias.

- Azure Application Gateway: Gerencia o tráfego de aplicativos com recursos como balanceamento de carga e firewall.

- Azure VPN Gateway: Conecta redes locais ao Azure por meio de uma VPN segura.

- Azure ExpressRoute: Proporciona conexões privadas e de baixa latência entre data centers locais e o Azure.

- Azure DNS: Gerenciamento de nomes de domínio e registros DNS.


Esses serviços de computação e rede no Azure garantem escalabilidade, segurança e alta disponibilidade, sendo essenciais para construir e operar aplicativos modernos e robustos na nuvem.

### Dominando o Armazenamento na Azure
Contas de Armazenamento no Azure
As Contas de Armazenamento no Azure são containers que gerenciam vários serviços de armazenamento: Blobs, Files, Queues e Tables. Principais peculiaridades:

Tipos: Standard (discos HDD, mais barato) e Premium (discos SSD, alta performance).
Redundância: Local (LRS), Zone (ZRS), Geo (GRS) e Read-Access Geo (RA-GRS).
Camadas de acesso: Hot (frequente), Cool (eventual) e Archive (raramente acessado).
Configurações importantes: Controle de acesso com RBAC (Role-Based Access Control), chaves de acesso, e SAS (Shared Access Signature) para links temporários.

Migrações para o Azure
O processo de migração envolve mover aplicativos, dados e infraestrutura local para a nuvem. Algumas estratégias comuns incluem:

Lift-and-Shift: Migração direta, sem modificações na arquitetura.
Replatform: Ajustes mínimos para aproveitar serviços PaaS do Azure.
Refactor/Rearchitect: Modificação completa do app para uma arquitetura nativa da nuvem.
Ferramentas: Azure Migrate é uma plataforma que auxilia em avaliações, planejamento e execução da migração.

AzCopy
O AzCopy é uma ferramenta de linha de comando poderosa para copiar dados entre contas de armazenamento no Azure ou entre o local e a nuvem.

Velocidade: Transferências rápidas, aproveitando paralelismo.
Casos de uso: Upload/download de Blobs, arquivos, e sincronização de diretórios.
Comandos úteis:
azcopy copy: Copiar arquivos entre fontes e destinos.
azcopy sync: Sincronizar diretórios entre a nuvem e local.
azcopy login: Autenticação segura com o Azure.

### Entendendo sobre Segurança e Identidade na Azure

- Azure AD (Entra ID)
O Entra ID (antigo Azure Active Directory) é o serviço de identidade e acesso do Azure. Ele autentica usuários e permite o controle de acesso a recursos na nuvem e em ambientes híbridos.

Suporte para SSO (Single Sign-On), autenticação multifator (MFA) e políticas de acesso condicional.
Integração com aplicativos SaaS e ambientes on-premises.

- Criação, Deleção e Convite de Usuários em Grupos
Criação/Deleção: Admins podem criar e remover usuários diretamente no Entra ID via portal, CLI ou PowerShell.
Convite: Usuários externos podem ser adicionados através de B2B (Business-to-Business), enviando convites por e-mail para colaborar com recursos específicos.
Grupos: Usados para organizar usuários e simplificar o gerenciamento de permissões.

- Sincronização de Usuários e Permissões (RBAC)
Azure AD Connect: Sincroniza usuários do Active Directory on-premises com o Entra ID para ambientes híbridos.
RBAC (Role-Based Access Control): Define permissões baseadas em funções (roles) atribuídas a usuários ou grupos, garantindo acesso apenas aos recursos necessários.

- Defender for Cloud
O Defender for Cloud é uma solução de segurança integrada que oferece:

Monitoramento contínuo de recursos na nuvem e recomendações de segurança.
Proteção contra ameaças para VMs, bancos de dados e contêineres.
Políticas de conformidade que ajudam a atender a padrões como ISO, GDPR e PCI-DSS.

- DevOps Security
Azure DevOps oferece integrações de segurança em pipelines CI/CD (integração e entrega contínuas).
Security Gates: Validações automáticas em código antes de produção.
DevSecOps: Práticas que integram segurança desde o início do desenvolvimento.
Ferramentas: Integração com GitHub Advanced Security e análise estática/dinâmica para detectar vulnerabilidades em código.

### Otimizando Custos no Azure

A otimização de custos no Azure busca reduzir despesas enquanto mantém a performance e a disponibilidade dos recursos. Algumas práticas recomendadas incluem:

-Reservas e Instâncias Spot: Descontos para workloads previsíveis e sob demanda (com risco de interrupção).

-Dimensionamento automático: Ajusta o uso de recursos conforme a demanda.

-Ajuste de recursos: Eliminar ou reduzir recursos subutilizados (direcionar para VMs menores, por exemplo).

-Monitoramento com Azure Cost Management: Analisar e definir alertas para gastos anormais.

-Políticas: Aplicação de políticas de Governança para evitar gastos fora do planejado.

Certificações sobre Otimização de Custos
-Microsoft Certified: Azure Fundamentals (AZ-900): Introduz conceitos de governança, faturamento e otimização de custos na nuvem.

-Microsoft Certified: Azure Administrator Associate (AZ-104): Foca em práticas de administração com módulos sobre monitoramento e controle de custos.

-Microsoft Certified: Azure Solutions Architect Expert (AZ-305): Explora otimização em arquitetura de soluções complexas e escaláveis.

-FinOps Certified Practitioner: Embora não específica do Azure, esta certificação ajuda a desenvolver habilidades de gestão financeira para múltiplas   nuvens.

### Gerenciando Politicas em Acessos Azure
-Portal de Confiança de Serviços (Microsoft Trust Center)
  O Portal de Confiança de Serviços é um repositório centralizado onde a Microsoft divulga informações sobre:

 - Segurança e privacidade dos serviços Azure e Microsoft 365.
 - Conformidade com regulamentações globais.
 - Transparência: Inclui relatórios de auditoria, termos de serviço e práticas de proteção de dados.
   
-Certificações, Padrões e Regulamentos

 - ISO/IEC 27001: Gestão de segurança da informação.
 - GDPR: Regulamento Geral de Proteção de Dados da União Europeia.
 - PCI DSS: Padrão para segurança de dados em pagamentos.
 - SOC 1, SOC 2, SOC 3: Relatórios de controles internos.
 
-Azure Purview
O Purview é uma solução de governança de dados e catalogação.

 - Descoberta e classificação: Identifica dados sensíveis automaticamente.
 - Mapeamento de linhagem de dados: Acompanhamento do fluxo de dados entre sistemas.
 - Catálogo de dados: Oferece uma visão unificada dos dados corporativos para facilitar a conformidade e otimização.

-Políticas no Azure
As Azure Policies permitem criar regras para garantir que os recursos estejam configurados de acordo com diretrizes específicas.

 - Governança automatizada: Aplicação de políticas para evitar desvios de conformidade.
 - Exemplos: Restringir tipos de VMs, exigir criptografia ou definir locais específicos para a criação de recursos.
 - Monitoramento: Assegura que recursos existentes também sigam essas políticas.

-Kubernetes no Azure (AKS)
O Azure Kubernetes Service (AKS) é uma plataforma gerenciada para a orquestração de contêineres.

 - Automação: Simplifica a implantação e o gerenciamento de clusters Kubernetes.
 - Escalabilidade: Suporta autoescalamento de cargas de trabalho.
 - Integração com DevOps e segurança: Oferece suporte a CI/CD, além de controle de acesso com RBAC e políticas de rede.

### Ferramentas de Implantação na Azure

-Criação de Recursos e Criação em Lote
 - Portal Azure: Interface gráfica para criar recursos de forma manual e rápida.
 - Automação em lote: Via scripts ou templates para implantar múltiplos recursos simultaneamente.
 - Escalabilidade: Ideal para grandes ambientes, reduzindo tempo e erros humanos.

-Azure Cloud Shell
 - Terminal integrado disponível diretamente no portal Azure.
 - Acessa ferramentas como CLI e PowerShell sem necessidade de instalação local.
 - Armazenamento persistente para scripts e arquivos no Azure Files.

-Azure CLI
 - Ferramenta de linha de comando multiplataforma.
 - Permite criar, atualizar e deletar recursos por meio de comandos simples.

-Bicep
 - Linguagem declarativa para infraestrutura como código (IaC), simplificando templates ARM (Azure Resource Manager). Mais fácil de ler e manter do que JSON.

-Azure Arc
 - Ferramenta que permite gerenciar recursos localizados fora do Azure (ambientes on-premises ou outras nuvens) como se estivessem no Azure.
 - Suporta servidores, contêineres e clusters Kubernetes externos.
 - Ideal para ambientes híbridos e multicloud, oferecendo governança e conformidade unificada.
