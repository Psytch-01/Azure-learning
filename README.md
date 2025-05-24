# ☁️ Estudos Azure

Este repositório reúne meus estudos sobre a plataforma Microsoft Azure. Aqui estão os principais conceitos que venho explorando até o momento, com anotações e observações feitas durante o aprendizado.

---

## 📌 Objetivo

Registrar meu progresso e fixar o conhecimento com base na prática e revisão dos conceitos. Este repositório pode ajudar outros iniciantes a entender os fundamentos da nuvem com Azure.  
Além de servir como Lab do Bootcamp Bradesco, na DIO.

---

## 📘 Conteúdos estudados

### → Conceitos básicos da computação em nuvem
- O que é computação em nuvem e como ela transforma o modo como lidamos com infraestrutura, desenvolvimento e serviços.  
- Vantagens como escalabilidade, alta disponibilidade e pagamento sob demanda.

---

### → Benefícios da nuvem
- **Alta disponibilidade**: os serviços na nuvem ficam no ar quase o tempo todo. O Azure garante isso por meio de SLAs — quanto maior o percentual, menor a chance de ficar indisponível.  
- **Escalabilidade**: posso aumentar os recursos (como CPU ou memória) automaticamente quando há mais demanda.  
- **Elasticidade**: dá pra aumentar ou reduzir recursos conforme o uso, sem pagar por algo que não estou usando.  
- **Confiabilidade**: a infraestrutura é feita para aguentar falhas, com sistemas de backup, redundância e recuperação.  
- **Previsibilidade**: consigo ter mais controle sobre os custos e desempenho, sem grandes surpresas.  
- **Segurança**: o Azure já traz várias camadas de proteção para dados, identidades, redes, etc.  
- **Governança**: dá pra criar políticas e regras de uso para manter o controle e evitar bagunça.  
- **Gerenciabilidade**: tem várias ferramentas que ajudam a monitorar, automatizar e administrar os recursos com mais facilidade.

---

### → CapEx vs OpEx
- **CapEx (Capital Expenditure)**: modelo de investimento com alto custo inicial em hardware e infraestrutura, que tende a diminuir despesas com o tempo.  
- **OpEx (Operational Expenditure)**: modelo usado na nuvem, baseado em custos operacionais, com pagamento por uso e maior flexibilidade.

---

### → Tipos de nuvem
- **Nuvem pública**: recursos compartilhados oferecidos por provedores como a Microsoft.  
- **Nuvem privada**: infraestrutura dedicada a uma única organização.  
- **Nuvem híbrida**: combinação entre nuvens públicas e privadas para maior controle e flexibilidade.

---

### → Modelos de serviço: IaaS, PaaS e SaaS
- **IaaS (Infrastructure as a Service)**: fornece infraestrutura sob demanda, como VMs, redes e armazenamento. O provedor gerencia o hardware e o cliente gerencia o sistema operacional, apps e dados. Ideal para quem precisa de controle total do ambiente.  
- **PaaS (Platform as a Service)**: oferece uma plataforma gerenciada para desenvolvimento e hospedagem de aplicações. O cliente foca apenas na aplicação e nos dados, enquanto o provedor cuida do restante. Indicado para desenvolvimento rápido e escalável.  
- **SaaS (Software as a Service)**: entrega softwares prontos via internet. O provedor é responsável por toda a estrutura, e o cliente apenas utiliza o serviço. Ex: Microsoft 365.

---

### → Componentes e arquitetura do Azure
O Azure é estruturado com **regiões geográficas**, **zonas de disponibilidade**, **grupos de recursos**, **assinaturas** e **serviços gerenciados**.  

A arquitetura é baseada em **distribuição global**, **redundância**, **segurança integrada** e **gestão centralizada** por meio do Azure Resource Manager (ARM).  

Os recursos são organizados logicamente para facilitar a governança e o controle de custos.

---

### → Regiões do Azure
**Região** é um conjunto geográfico de datacenters interconectados, onde os serviços do Azure são executados.  
Exemplos: *Brazil South*, *East US*, *West Europe*.

---

### → Pares de regiões
O Azure organiza algumas regiões em **pares** (*region pairs*) para replicação e recuperação de desastres.  
Ex: *Brazil South* é pareada com *South Central US*.  
Os pares garantem atualizações ordenadas e alta disponibilidade entre locais geograficamente próximos.

---

### → Regiões soberanas
São regiões **isoladas da nuvem pública**, criadas para atender requisitos regulatórios e de conformidade específicos.  
Ex: *Azure Government* (EUA), *Azure China* (operado por parceiro local).

---

### → Grupo de recursos
**Resource Group** é uma unidade lógica que agrupa recursos relacionados de um projeto.  
Serve para organizar, gerenciar e aplicar políticas de forma centralizada.  
Ex: VMs, bancos de dados e redes de um mesmo sistema podem estar no mesmo grupo.

---

### → Tipos de assinaturas no Azure
A **assinatura** no Azure é a unidade lógica de cobrança, gerenciamento e organização dos recursos. Por meio dela, é possível distribuir e controlar o acesso de diferentes equipes ou ambientes.  

Cada assinatura pode conter múltiplos usuários com diferentes níveis de permissão (via Azure Active Directory), e ser usada para separar:  
- Ambientes (produção, desenvolvimento, testes)  
- Equipes (equipe de dev, equipe de QA, equipe de operações)  
- Projetos ou departamentos distintos  

Isso facilita a **organização**, o **controle de custos** e a **aplicação de políticas específicas** para cada área.  

Além disso, uma única conta pode ter acesso a várias assinaturas, e elas podem ser agrupadas em **tenants** para gerenciamento centralizado.

---

### → Principais serviços e ferramentas do Azure
- **Azure Portal**: interface gráfica para gerenciar recursos.  
- **Azure CLI**: ferramenta de linha de comando para automação e administração.  
- **Máquinas Virtuais (VMs)**, **App Services**, **Storage Accounts**, **Azure SQL Database**, entre outros serviços fundamentais.

---

### → Computação e Rede no Azure

#### Máquinas Virtuais (Virtual Machines - VMs)
Serviço de **IaaS (Infrastructure as a Service)** que permite criar e gerenciar servidores virtuais no Azure. Ideal para quando é necessário controle total do sistema operacional e ambiente de execução. As VMs podem ser utilizadas para hospedar aplicações, bancos de dados ou sistemas legados.

#### Conjuntos de Disponibilidade (Availability Sets)
Recurso de alta disponibilidade para VMs. Distribui instâncias entre domínios de falha e atualização, garantindo que falhas físicas ou manutenções planejadas não afetem todas as instâncias ao mesmo tempo. É uma prática comum em arquiteturas resilientes.

#### Área de Trabalho do Azure (Azure Virtual Desktop)
Serviço de **DaaS (Desktop as a Service)**, que permite publicar áreas de trabalho e aplicativos para acesso remoto, com segurança e escalabilidade. Usuários podem acessar seus ambientes de trabalho a partir de qualquer lugar, com gerenciamento centralizado.

#### Contêineres no Azure
O Azure oferece suporte a contêineres, que permitem empacotar aplicações com suas dependências de forma leve e portátil.  

- **Azure Container Instances (ACI)** – Serviço de **PaaS**, ideal para executar contêineres de forma rápida e sob demanda, sem necessidade de orquestração.  
- **Azure Kubernetes Service (AKS)** – Plataforma de **PaaS** para orquestração de contêineres usando Kubernetes. Gerencia clusters com escalabilidade, automação e integração nativa ao ecossistema Azure.

#### Azure Functions
Serviço de **PaaS** para execução de funções serverless. Permite rodar trechos de código em resposta a eventos (como requisições HTTP ou alterações em banco de dados), com cobrança baseada no tempo de execução. Ótimo para automações e tarefas pontuais.

#### Gateway de Aplicativo (Application Gateway)
Serviço de **PaaS** que atua como um balanceador de carga de nível 7 (camada de aplicação). Permite gerenciamento de tráfego, SSL offload, roteamento baseado em URL e proteção contra ataques com Web Application Firewall (WAF).

#### VPN Gateway
Serviço de **PaaS** que estabelece conexões seguras entre a rede local (on-premises) e a rede virtual no Azure, usando IPsec/IKE. Utilizado para comunicação privada e segura com recursos hospedados na nuvem.

#### Azure ExpressRoute
Solução de conectividade privada entre a infraestrutura local e o Azure, sem passar pela internet pública. Proporciona maior confiabilidade, baixa latência e segurança. Classificado como **PaaS** voltado para conexões corporativas de alta performance.

#### DNS do Azure (Azure DNS)
Serviço de **PaaS** que permite hospedar zonas DNS e gerenciar nomes de domínio com alta disponibilidade e baixa latência. Integrado com o Azure Resource Manager, facilita a automação e a governança dos registros DNS.

---

### → Tipos de Inteligência Artificial (IA)

O Azure oferece uma gama de serviços de IA para diferentes finalidades, que se encaixam em várias categorias. Cada tipo resolve problemas específicos com abordagens distintas:

#### 📈 Machine Learning (Aprendizado de Máquina)
Permite que sistemas aprendam com dados e façam previsões ou classificações sem serem explicitamente programados.  
Com o **Azure Machine Learning**, é possível treinar, implantar e monitorar modelos com automação e suporte a diversas linguagens como Python e R.

#### 🗣️ Processamento de Linguagem Natural (PLN)
Focado em fazer com que máquinas compreendam, interpretem e gerem linguagem humana.  
Serviços como o **Azure Language Service** permitem detectar sentimentos, extrair palavras-chave, identificar entidades e traduzir idiomas com alta precisão.

#### 🧾 Inteligência de Documentos (Document Intelligence)
Automatiza a leitura, interpretação e extração de dados estruturados a partir de documentos não estruturados, como PDFs, imagens escaneadas e formulários.  
O **Azure AI Document Intelligence (antigo Form Recognizer)** é usado para digitalizar e entender faturas, contratos, recibos, entre outros.

#### 🧠 Mineração de Conhecimento
Relaciona dados dispersos em informações úteis, conectando entidades, padrões e relações entre conteúdos.  
Com ferramentas como **Azure Cognitive Search**, é possível criar experiências de busca inteligente com filtros, sugestão automática e enriquecimento semântico.

#### 🎨 IA Generativa
Capaz de criar conteúdo original — como texto, imagem, áudio ou código — a partir de comandos simples.  
O **Azure OpenAI Service** oferece acesso a modelos como GPT (da OpenAI), permitindo construir assistentes virtuais, geradores de texto, resumos automáticos e soluções criativas personalizadas.

Esses recursos permitem integrar IA em sistemas de forma modular e escalável, sem a necessidade de criar modelos do zero.

---

### → Princípios de IA Responsável

Ao trabalhar com Inteligência Artificial, especialmente em ambientes corporativos e de larga escala como o Azure, é essencial adotar princípios de **IA responsável**. A Microsoft segue uma base ética para o desenvolvimento e uso de IA, visando o impacto positivo da tecnologia na sociedade. Os principais pilares são:

#### ⚖️ Imparcialidade
A IA deve tomar decisões justas e sem preconceitos. Isso exige atenção especial na coleta, preparo e balanceamento dos dados para evitar vieses que possam prejudicar grupos ou indivíduos. Modelos precisam ser avaliados continuamente quanto à equidade de suas previsões.

#### 🔐 Privacidade e Segurança
A IA deve proteger a confidencialidade das informações, seguindo leis como a LGPD e o GDPR. Dados pessoais usados para treinar modelos precisam ser anonimizados, armazenados com segurança e acessados apenas quando necessário. A arquitetura da solução também deve garantir proteção contra vazamentos e acessos não autorizados.

#### 🤝 Confiabilidade e Confiança
Modelos de IA devem funcionar com consistência, mesmo em situações imprevistas. Isso exige testes rigorosos, validação constante e transparência nos limites da tecnologia. O comportamento dos sistemas deve ser previsível e compreensível para os usuários.

#### 🌐 Inclusão
A IA deve ser desenvolvida com foco na diversidade, atendendo às necessidades de diferentes perfis, idiomas, culturas e capacidades. Um sistema realmente inclusivo considera acessibilidade desde o design, para que mais pessoas possam interagir com ele de forma igualitária.

#### 🔎 Transparência
Os usuários devem entender como e por que a IA toma determinadas decisões. Isso inclui fornecer explicações claras sobre o funcionamento dos modelos e tornar acessível o raciocínio por trás das recomendações ou classificações feitas pelo sistema.

#### 🧭 Responsabilidade
Quem cria ou utiliza IA deve ser responsável pelos resultados gerados. Isso significa assumir a supervisão humana, aplicar mecanismos de correção e estar preparado para intervir caso algo saia do controle. A IA é uma ferramenta poderosa, mas não pode substituir o julgamento ético humano.

Esses princípios ajudam a garantir que o uso de IA seja benéfico, confiável e alinhado aos valores humanos — algo fundamental à medida que essas tecnologias se tornam mais presentes na vida real.

---

### → Processamento de Linguagem Natural (PLN) Aprofundado

O **Processamento de Linguagem Natural (PLN)** é uma área da Inteligência Artificial focada em permitir que computadores compreendam, interpretem, analisem e gerem a linguagem humana de forma significativa. Ele é fundamental para construir aplicações como assistentes virtuais, mecanismos de busca, análise de sentimentos, tradutores automáticos, entre outros.

No contexto corporativo, o PLN ajuda empresas a extrair valor de grandes volumes de dados textuais, automatizar interações com clientes e tomar decisões mais rápidas com base em informações não estruturadas.

#### 🧠 Exemplos de tarefas de PLN:
- **Análise de sentimentos**: entender se uma mensagem tem tom positivo, negativo ou neutro.
- **Extração de entidades**: identificar nomes de pessoas, locais, datas e outros termos relevantes.
- **Resumo de textos**: gerar versões reduzidas com as informações principais.
- **Classificação de tópicos**: categorizar documentos automaticamente com base no conteúdo.
- **Tradução automática**: converter textos entre diferentes idiomas.
- **Chatbots e assistentes virtuais**: interagir em linguagem natural com usuários.

#### 🛠️ Ferramentas do Azure para PLN:
- **Azure AI Language (anteriormente Text Analytics)**: oferece APIs prontas para análise de sentimentos, extração de entidades, detecção de idioma, classificação de texto, entre outros.
- **Azure OpenAI Service**: acesso a modelos avançados de linguagem, como GPT (usado aqui neste markdown!), para criação de resumos, geração de texto, tradução, reescrita, entre outras tarefas.
- **Azure Bot Service**: permite criar chatbots inteligentes com suporte a linguagem natural, integrando com o LUIS (Language Understanding Intelligent Service).
- **Azure Cognitive Search**: utiliza PLN para enriquecer buscas em grandes conjuntos de dados com linguagem natural e inteligência semântica.

Essas ferramentas são altamente escaláveis, com suporte multilíngue e integração facilitada com outros serviços do Azure. Assim, desenvolvedores e empresas conseguem incluir inteligência linguística em suas aplicações de forma segura, eficiente e produtiva.

--- 

### → Inteligência de Documentos e Mineração de Conhecimento

#### Inteligência de Documentos (Document Intelligence)

O Azure oferece soluções avançadas para extrair automaticamente informações relevantes de documentos estruturados e não estruturados, como faturas, recibos, formulários, contratos e muito mais.

- **Azure AI Document Intelligence (antigo Form Recognizer)**: Serviço de **IA aplicada a documentos**, que usa modelos pré-treinados ou personalizados para extrair textos, tabelas, campos-chave e estrutura de documentos.  
Ideal para automatizar processos manuais e reduzir o tempo de análise de documentos.

Principais recursos:
- Extração de texto via OCR de alta precisão;
- Reconhecimento de campos específicos (como valores, datas, IDs);
- Treinamento com seus próprios documentos;
- Suporte a múltiplos formatos: PDF, JPG, PNG, entre outros.

Casos de uso incluem:
- Processamento automático de faturas;
- Análise de contratos;
- Digitalização de formulários de entrada de dados.

#### Mineração de Conhecimento

A mineração de conhecimento no Azure está ligada à **capacidade de organizar, explorar e gerar valor a partir de grandes volumes de informação** (estruturada ou não), conectando dados dispersos e promovendo insights automáticos.

Ferramentas relacionadas:

- **Azure AI Search** (anteriormente Azure Cognitive Search): motor de busca inteligente com IA integrada. Pode aplicar análise semântica, reconhecimento de linguagem natural e filtros personalizados em grandes bases de dados.  
Permite adicionar funcionalidades de busca com compreensão contextual a aplicações, portais ou sistemas internos.

- **Semantic Ranker e Respostas Inteligentes**: Camadas adicionais que enriquecem os resultados da busca com compreensão de intenção e linguagem, otimizando a experiência do usuário com respostas mais relevantes.

- **Integration com o Azure OpenAI + Search**: É possível combinar a capacidade de indexação do AI Search com a linguagem natural do ChatGPT, criando **experiências de pergunta e resposta sobre seus próprios dados**.

Essa combinação permite **conversar com documentos** de forma dinâmica, transformando repositórios em fontes de conhecimento interativo.

---

Essas soluções elevam o potencial de uso de informações armazenadas em documentos, bancos de dados e arquivos, promovendo eficiência, automação e descoberta de conhecimento com apoio da Inteligência Artificial.

---
---

### → IA Generativa e Modelos de Linguagem

#### Modelos de Linguagem de Grande Escala (LLMs)

Modelos de Linguagem de Grande Escala, conhecidos como **LLMs (Large Language Models)**, são redes neurais treinadas com enormes volumes de texto para entender, gerar e manipular linguagem humana. Esses modelos são a base da **IA generativa**, permitindo que sistemas criem textos, códigos, resumos, traduções, entre outras tarefas linguísticas.

Esses modelos funcionam com base em dois componentes principais:

- **Codificador (Encoder)**: responsável por entender o contexto de entrada — por exemplo, uma pergunta ou um comando. Ele transforma o texto em vetores numéricos (tokens) que representam semanticamente as palavras.
- **Decodificador (Decoder)**: usa esses vetores para gerar uma resposta coerente e contextualizada.

Outros conceitos fundamentais incluem:

- **Tokenização**: o texto é dividido em partes menores (tokens), como palavras ou subpalavras, que são processadas pelos modelos.
- **Inserções (Insertions)**: os modelos podem completar ou inserir texto em pontos específicos, mantendo o contexto antes e depois.
- **Mecanismo de Atenção (Attention)**: técnica que permite ao modelo focar nas partes mais relevantes do texto de entrada, capturando relações contextuais mesmo entre palavras distantes no texto.

Esse conjunto de técnicas permite à IA gerar conteúdo de maneira natural e útil, com base em comandos simples dados pelos usuários.

---

### → Copilots: IA integrada às aplicações

**Copilots** são aplicações de IA generativa integradas a ferramentas do dia a dia, como editores de texto, planilhas, plataformas de desenvolvimento, sistemas de atendimento, entre outros.

Eles atuam como **assistentes contextuais**, capazes de:

- Responder perguntas com base nos dados da aplicação.
- Gerar e resumir conteúdos.
- Automatizar tarefas repetitivas.
- Aumentar a produtividade e reduzir erros operacionais.

Um exemplo notável é o **Microsoft 365 Copilot**, que combina LLMs com dados da organização (e-mails, documentos, chats) para fornecer respostas personalizadas e relevantes.

---

### → Azure OpenAI Service

O **Azure OpenAI Service** disponibiliza os modelos da OpenAI (como GPT-4, Codex e DALL·E) com a infraestrutura e a segurança da nuvem da Microsoft.

Com ele, é possível integrar **IA generativa de alto desempenho** às aplicações empresariais, mantendo o controle de privacidade e governança sobre os dados.

Entre suas funcionalidades, estão:

- Geração de texto, resumo, tradução e classificação.
- Geração e explicação de código.
- Análise semântica de dados e documentos.
- Criação de chatbots com linguagem natural.

Esse serviço também pode ser combinado com **Azure Cognitive Search**, **Azure AI Studio** e **Azure Machine Learning**, ampliando as possibilidades de construção de soluções inteligentes e escaláveis.

---

## 🛠️ Em breve...

Novos conteúdos serão adicionados conforme avanço nos estudos.
