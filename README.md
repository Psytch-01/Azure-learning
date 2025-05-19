# ☁️ Estudos Azure

Este repositório reúne meus estudos sobre a plataforma Microsoft Azure. Aqui estão os principais conceitos que venho explorando até o momento, com anotações e observações feitas durante o aprendizado.

## 📘 Conteúdos estudados

### → Conceitos básicos da computação em nuvem
- O que é computação em nuvem e como ela transforma o modo como lidamos com infraestrutura, desenvolvimento e serviços.
- Vantagens como escalabilidade, alta disponibilidade e pagamento sob demanda.

### → Benefícios da nuvem
- Alta disponibilidade: os serviços na nuvem ficam no ar quase o tempo todo. O Azure garante isso por meio de SLAs — quanto maior o percentual, menor a chance de ficar indisponível.  
- Escalabilidade: posso aumentar os recursos (como CPU ou memória) automaticamente quando há mais demanda.  
- Elasticidade: dá pra aumentar ou reduzir recursos conforme o uso, sem pagar por algo que não estou usando.  
- Confiabilidade: a infraestrutura é feita para aguentar falhas, com sistemas de backup, redundância e recuperação.  
- Previsibilidade: consigo ter mais controle sobre os custos e desempenho, sem grandes surpresas.  
- Segurança: o Azure já traz várias camadas de proteção para dados, identidades, redes, etc.  
- Governança: dá pra criar políticas e regras de uso para manter o controle e evitar bagunça.  
- Gerenciabilidade: tem várias ferramentas que ajudam a monitorar, automatizar e administrar os recursos com mais facilidade.

### → CapEx vs OpEx
- **CapEx (Capital Expenditure)**: modelo de investimento com alto custo inicial em hardware e infraestrutura, que tende a diminuir despesas com o tempo. 
- **OpEx (Operational Expenditure)**: modelo usado na nuvem, baseado em custos operacionais, com pagamento por uso e maior flexibilidade.

### → Tipos de nuvem
- **Nuvem pública**: recursos compartilhados oferecidos por provedores como a Microsoft.
- **Nuvem privada**: infraestrutura dedicada a uma única organização.
- **Nuvem híbrida**: combinação entre nuvens públicas e privadas para maior controle e flexibilidade.

### → Modelos de serviço: IaaS, PaaS e SaaS
- IaaS (Infrastructure as a Service): fornece infraestrutura sob demanda, como VMs, redes e armazenamento. O provedor gerencia o hardware e o cliente gerencia o sistema operacional, apps e dados. Ideal para quem precisa de controle total do ambiente.
 
- PaaS (Platform as a Service): oferece uma plataforma gerenciada para desenvolvimento e hospedagem de aplicações. O cliente foca apenas na aplicação e nos dados, enquanto o provedor cuida do restante. Indicado para desenvolvimento rápido e escalável.

- SaaS (Software as a Service): entrega softwares prontos via internet. O provedor é responsável por toda a estrutura, e o cliente apenas utiliza o serviço. Ex: Microsoft 365.

### → Componentes e arquitetura do Azure  
O Azure é estruturado com **regiões geográficas**, **zonas de disponibilidade**, **grupos de recursos**, **assinaturas** e **serviços gerenciados**.

A arquitetura é baseada em **distribuição global**, **redundância**, **segurança integrada** e **gestão centralizada** por meio do Azure Resource Manager (ARM).

Os recursos são organizados logicamente para facilitar a governança e o controle de custos.

### → Regiões do Azure  
**Região** é um conjunto geográfico de datacenters interconectados, onde os serviços do Azure são executados.  
Exemplos: *Brazil South*, *East US*, *West Europe*.

### → Pares de regiões  
O Azure organiza algumas regiões em **pares** (*region pairs*) para replicação e recuperação de desastres.  
Ex: *Brazil South* é pareada com *South Central US*.  
Os pares garantem atualizações ordenadas e alta disponibilidade entre locais geograficamente próximos.

### → Regiões soberanas  
São regiões **isoladas da nuvem pública**, criadas para atender requisitos regulatórios e de conformidade específicos.  
Ex: *Azure Government* (EUA), *Azure China* (operado por parceiro local).

### → Grupo de recursos  
**Resource Group** é uma unidade lógica que agrupa recursos relacionados de um projeto.  
Serve para organizar, gerenciar e aplicar políticas de forma centralizada.  
Ex: VMs, bancos de dados e redes de um mesmo sistema podem estar no mesmo grupo.

### → Tipos de assinaturas no Azure  
A **assinatura** no Azure é a unidade lógica de cobrança, gerenciamento e organização dos recursos. Por meio dela, é possível distribuir e controlar o acesso de diferentes equipes ou ambientes.

Cada assinatura pode conter múltiplos usuários com diferentes níveis de permissão (via Azure Active Directory), e ser usada para separar:

- Ambientes (produção, desenvolvimento, testes)  
- Equipes (equipe de dev, equipe de QA, equipe de operações)  
- Projetos ou departamentos distintos

Isso facilita a **organização**, o **controle de custos** e a **aplicação de políticas específicas** para cada área.

Além disso, uma única conta pode ter acesso a várias assinaturas, e elas podem ser agrupadas em **tenants** para gerenciamento centralizado.

### → Principais serviços e ferramentas do Azure
- **Azure Portal**: interface gráfica para gerenciar recursos.
- **Azure CLI**: ferramenta de linha de comando para automação e administração.
- **Máquinas Virtuais (VMs)**, **App Services**, **Storage Accounts**, **Azure SQL Database**, entre outros serviços fundamentais.

---

## 📌 Objetivo

Registrar meu progresso e fixar o conhecimento com base na prática e revisão dos conceitos. Este repositório pode ajudar outros iniciantes a entender os fundamentos da nuvem com Azure.  
Além de servir como Lab do Bootcamp Bradesco, na DIO.

---

## 🛠️ Em breve...

Novos conteúdos serão adicionados conforme avanço nos estudos.
