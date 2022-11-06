# Tecnologia

- Tecnologia é a parte mais importante do exame, consistindo de aproximadamente um terço da sua pontuação geral. 
- **Definição:** Ao dizer *tecnologia*, estamos nos referindo aos vários tipos de serviços, infraestrutura e aspectos operacionais do uso da AWS.

### Defina os métodos de implantação e operação na AWS
-  Neste tema, falaremos sobre diferentes formas de operação, tipos de modelos de implantação, opções de conectividade.

- Existem diversos métodos que podem ser utilizados para se comunicar com a AWS para provisionamento e operações necessárias que você pode precisar gerenciar. Estes são:
  - Acesso programáticos às APIs por meio de SDKs;
  - Acesso através da *AWS Command Line Interface (AWS CLI)*;
  - Acesso através do *AWS Management Console*;
  - Criar e implementar com várias ferramentas de *Infrastructure as Code (IAC)*.  

- Alem de conhecer esses métodos de comunicação, saber quais são os pontos fortes e fracos de cada um deles.

- Modelos de implantação na nuvem, ou seja, métodos de utilização da Cloud. **Isto não é sobre implantação de código.** Estes métodos são:
  - Nativo da núvem (ou integral com a nuvem);
  - Hibrido;
  - On-Premises (Local);
- Assim como antes, é importante saber quando estes métodos de utilização podem ser utilizados na prática.
- **Exemplo:** Os aplicativos executados em conjunto pelo seu data center on-premises e a AWS são implantações hibridas ou on-premises?
- Quais são as considerações que precisam ser observadas ao usar os diferentes tipos de implantações.

- Opçoes de Conectividade. Estas opções são formas de gerenciar a conectividade de rede em vários serviços da AWS e incluem:
  -  Rede privada virtual (VPN);
  -  AWS DirectConnect;
  -  Rede pública.


#### Question Walkthrough
**Pergunta:** Quais componentes **são necessários** para criar uma conexão **Site-to-Site VPN** bem sucedida na AWS? (Seleciona DUAS respostas).
- A) Gateway de Internet;
- B) NAT Gateway;
**- C) Gateway do cliente;**
- D) Transit Gateway;
**- E) Virtual private gateway.**
  
### Defina a infraestrutura global da AWS.
- Neste tema, falaremos sobre os vários componentes que formam nossa infraestrutura global, tais como as Zonas de Disponibildiade, Regiões e locais de borda.

- Quando falamos da **Infraestrutura Global**, estamos falando especificamente de:
  - Zonas de Disponiblidades (AZ);
  - Regiões;
  - Locais de Borda (Edge Locations).
- É necessário entender a relação entre eles.
  - Como eles se encaixam no contexto da sua arquitetura?
  - Como eles funcionam individualmente e em conjunto?
  - Como você determina quando os serviços devem usar uma AZ, Região ou local de borda?

- Falando sobre **Zonas de disponibilidade**:
  - Saber quais serviços são limitados por seus limites e como as AZs podem te ajudar a criar um ambiente altamente disponível.
  - Entender como as AZs se comportam quando você está determinando pontos de falha nas suas arquiteturas;
  - Como a comunicação é feita ao ir de uma AZ para outra?
  - **Isso muda de serviço para serviço**, então você precisa saber quais serviços lidam especialmente com AZs e como eles se comunicam através de AZs.

- Falando sobre **Regiões**: *Locais físicos ao redor do mundo onde a AWS mantém seus clusters de data centers*.
  - Analisar os mesmos items que nas AZs;
  - Procure maneiras de usar regiões na recuperação de desastres e continuidade de negócio;
  - O que você pode fazer para evitar falhas catastróficas e quais serviços ajudam você a usar regiões?
  - Entender quando usar diferentes regiões e quais são os benefícios do uso de uma região específica ou do uso de várias regiões.
  - Veja como o uso de regiões afeta seus requisitos de compliance. **Frequentemente, o gerenciamento de dados é determinado por fronteiras soberanas.** É importante saber como essas leis e requisitos afetarão seu uso da AWS Cloud.

- Falando sobre **Locais de borda**: *endpoints que veiculam conteúdo armazenado em cache e dão acesso a serviços da AWS.*
  - Entender quais serviços se utilizam de locais de borda e qual a diferença de uso nesses serviços;
  - Você pode escolher quais locais de borda usar?
  - Como os locais de borda são usados no Amazon Cloud Front? E no AWS Global Accelerator? Os locais de borda são usados apenas nesses serviços?
  - Quais benefícios são fornecidos pelos locais de borda e qual o nível de gerenciamento pode ser imposto?

**Zonas de disponibilidade, regiões e locais de borda são componentes cruciais para entender e usar a AWS.**

#### Question Walkthrough
**Pergunta:** Qual é o aspecto da infraestrutura da AWS que **permite a implantação global de computação e de armazenamento**?
**Respostas:**
- A) Zonas de Disponibilidade; - *São um ou mais data centers distintos com energia, rede e conectividade redundantes em um região da AWS*. Elas permitem que você obtenha uma implantação altamente disponível em uma dada região mas elas não fornecem uma implantação global.
- **B) Regiões;**
- C) Tags; - *São metadados associados aos recursos. Elas ajudam a gerenciar recursos com algum esforço adicional, mas não permitem a implantação global dos seus recursos.*
- D) Resource Groups - *Pode facilitar o gerenciamento de recursos mas não permite a implantação de recursos da AWS globalmente.*

### Identificar os principais serviços da AWS.
- Neste tema, falaremos sobre as principais categorias de serviços e exemplos de cada.

- As principais categorias de serviços da AWS são: **Computação, Armazenamento, redes e banco de dados.**
- Estes são alguns pontos em comum entre todas as categorias e precisam ser entendidos:
  - Saiba como classificar os serviços da AWS em categorias.
    - O que faz com que um serviço seja de **computação** ou de **banco de dados**?
  - Saiba porque escolher serviços em categorias diferentes.
    - Quando você deve escolher um serviço de banco de dados em vez de executar um banco de dados em uma instância EC2?
  - Quais subcategorias existem nas categorias de serviços maiores?
    - Existem diferentes tipos de armazenamento?

- Falando sobre **Computação**:
  - Primeiramente, você precisa saber que existem diferentes famílias, ou tipos, de instâncias.
    - Saiba mais sobre os motivos para escolher instâncias de diferentes tipos de famílias, como elas funcionam e quais limitações podem ter.
  - Além das instâncias EC2, quais outros serviços estão disponíveis? Eles funcionam da mesma forma? 
  - Como diferentes serviços integram? Como personlização afetam isso?
  - Ser capaz de implementar elasticidade nos serviços computacionais além de desacoplamento.
  - **Pode haver diferentes maneiras ou serviços usados para gerenciar essas tarefas e seu nível de controle pode variar.**
  - A computação abrange muitos serviços diferentes. Independente de você trabalhar com funções no **AWS Lambda**, stacks de aplicativo no **AWS Elastic Beanstalk**, gerenciamento de contêiner no **AWS Elastic Container Service** ou utilizando **EC2**, existem muitas opções de computação na AWS.
  - **O guia do exame lista vários dos serviços computacionais, então certifique se você está analisando todos eles e não só o EC2.**

- Falando sobre **Armazenamento**:
  - É importante analisar não só como os serviços operam e as limitações deles, mas também o uso real deles.
    - Quais são as limitações de armazenamento?
    - Como o acesso do Amazon Elastic Block Store (EBS) é diferente do Amazon Simple Storage Service (S3);
    - Quais são algumas das considerações a fazer ao decidir se você usará o S3, o EBS, S3 Glacier ou Amazon Elastic File System (EFS)?
    - Como são transferência de dados com diversas quantidades de dados, seja transferindo arquivos específicos ou conjunto de arquivos inteiros?

- Falando sobre **Redes**:
  - Se trata do controle e otimização de acesso e comunicação.
  - Veja com o Amazon Virtual Private Cloud (VPC) ajuda você a controlar acesso aos seus recursos;
  - Como você pode aproveitar os recursos, controle e configurações para aumentar a privacidade e segurança dos seus ambientes?
  - O que você pode fazer para fornecer conectividade às VPCs a partir da internet ou localmente?
  - Como criar conexões entre localizações locais e na AWS.
  - Avalie itens como a criação de VPN e o possível uso do AWS Direct Connect;
  - Entenda como o Amazon Route 53 pode se encaixar. Apesar de ser um serviço DSN, ele fornece muitas funcionalidades quando se trata de gerenciar a conectividade e comunicação nos e entre seus ambientes.
    - Entenda seus recursos e quando esses recursos podem ser usados nos seus casos de uso.

- Falando sobre **Banco de Dados**:
  - Diferenciar quais serviços se encaixam em cenários específicos. Isso envolver comparar serviços como **Amazon RDS**, **Amazon DynamoDB** e **Amazon Redshift** entre si. Além de compará-los com o gerenciamento do seu banco de dados em instâncias do EC2.
  - Quais vantagens você obtém ao usar o serviço gerenciado?
  - Como a utilização de serviços gerenciados difere de um mecanismo de banco de dados instalado em uma instância, quando se trata de personalização, gerenciamento e desempenho?
  - Quais são as limitações de cada estilo de banco de dados?
  - É importante observar não apenas a variedade de serviços gerenciados mas também os vários níveis de gerenciamento que eles fornecem.
  - Da mesma forma que o **DynamoDB** e o **RDS** são gerenciados de modo diferente, também varia quando se olha o **Amazon Kubernetes Service (EKS)**, o **AWS Fargate** entre outros.

#### Question Walkthrough
**Pergunta:** Qual é o serviço da AWS **MAIS eficiente para importar exabytes de dados de um ambiente on-premises para a AWS Cloud?**
**Resposta:**
- **A) AWS Snowmobile;** - *Projetado especificamente para transferencia de daos em escala de exabytes.*
- B) AWS Storage Gateway;
- C) AWS Snowball;
- D) AWS Direct Connect


### Recursos para suporte à tecnologia.
- Neste, falaremos sobre documentação, níveis de suporte e outros serviços associados ao suporte à utilização da tecnologia da AWS.

- Quando você deparar com algo que não sabe ou precisar de algo que seria muito dificil ou demorado para criar você mesmo, existem várias opções para suporte à tecnologia.
- Neste contexto, suporte não siginifica apenas algo que deu errado e você precisa de ajuda para corrigi-lo.
- O suporte pode incluir **auxílio no projeto, orientação na arquitetura, resolução de problemas e colaboração da comunidade.**
- Quando considerar suporte no exame, existem aspectos que você deve avaliar:
  - Primeiramente, considere a ampla documentação existente, como foruns, whitepapers, blos e todas as áreas de documentação da AWS;
    - Onde você deve ir se precisar de instruções guiadas sobre como implantar um serviço pela primeira vez?
    - O que acessar se você estiver procurando práticas recomendadas?
    - Como buscar apoio da comunidade quando tem uma pergunta muito específica sobre o que você está criando?
  - Suporter específico da conta.
    - Avalie como você pode usar as várias equipes no **AWS Abuse** no **Suporte Premium** e no **Suporte de Cobrança e Conta**.
  - Quando você pode usar **Techinical Account Managers** e como eles podem ajudar seu ambiente?
- Entenda que o **AWS Partner Network** está disponível para ser usado.
  - Saber o que é, o que pode ser encontrado, possíveis limitações e os benefícios do uso do APN;
- Por último, não se esqueça do **AWS Trusted Advisor**, entenda o que ele faz, como ele pode ajudar você e quais informações estão disponíveis.

#### Question Walkthrough
**Pergunta:** **Qual plano de suporte da AWS** dá acesso a **revisões operacionais e de arquitetura,** além de **acesso 24h a engeheiros-sênior de suporte de nuvem por email, chat on-line e telefone**?
- A) Basic - *Disponível para todos os clientes da AWS. Fornece acesso a várias páginas de documentação e recursos, mas não atende os requisitos desejados.*
- B) Business - *Fornece acesso 24h aos engenheiros de suporte à nuvem, mas não inclui engenheiros senior ou outros requisitos desejados*.
- C) Developer - *Fornece acesso apenas durante o horário comercial.*
- **D) Enterprise**

### Domain Notes:
- Com o crescimento da popularidade da computação em nuvem, vários modelos e estratégias de implantação diferentes surgiram para atender a essas necessidades específicas de usuários distintos. Cada tipo de serviço de nuvem e método de implantação disponibiliza diferentes níveis de controle, flexibilidade e gerenciamento. A compreensão das diferenças entre a infraestrutura como um serviço (IaaS), a plataforma como um serviço (PaaS) e o software como um serviço (SaaS), assim como as estratégias de implantação que você pode utilizar, pode ajudar você a decidir qual conjunto de serviços é o ideal para as suas necessidades.

  Saiba mais em: [Tipos de computação em nuvem](https://aws.amazon.com/types-of-cloud-computing/)

- Os serviços de nuvem híbrida da AWS oferecem uma experiência da AWS consistente da maneira que você precisar: seja na nuvem, on-premises ou na borda. Você pode selecionar entre um amplo conjunto de serviços de computação, redes, armazenamento, segurança, identidade, integração de dados, gerenciamento, monitoramento e serviços de operações para criar arquiteturas híbridas que atendam às suas necessidades específicas e casos de uso.

  Saiba mais em: [Nuvem híbrida com a AWS](https://aws.amazon.com/hybrid/)

- O Amazon Virtual Private Cloud (Amazon VPC) fornece várias opções de conectividade de rede para você usar, de acordo com os requisitos e designs de rede atuais. Essas opções de conectividade incluem o uso da Internet ou de uma conexão do AWS Direct Connect como backbone da rede e o encerramento da conexão na AWS ou em endpoints de rede gerenciados pelo usuário. Além disso, com a AWS, você pode escolher como o roteamento de rede é entregue entre o Amazon VPC e suas redes usando serviços da AWS ou equipamentos e rotas de rede gerenciados pelo usuário.

  Saiba mais lendo o seguinte whitepaper da AWS: [Opções de conectividade do Amazon Virtual Private Cloud](https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/introduction.html)


- A infraestrutura de nuvem global da AWS é uma plataforma de nuvem segura, abrangente e confiável que oferece mais de 200 serviços em destaque de data centers em todo o mundo. Se você precisa implantar workloads de aplicativos em todo o mundo com um único clique ou criar e implantar aplicativos específicos mais próximos dos usuários com uma latência inferior a 10 milissegundos, a AWS fornece a infraestrutura de nuvem onde e quando você precisar.

  Saiba mais em: [Infraestrutura global](https://aws.amazon.com/about-aws/global-infrastructure/)

- A AWS oferece um amplo conjunto de produtos globais baseados na nuvem, incluindo computação, armazenamento, rede e bancos de dados. Esses serviços ajudam as organizações a se mover mais rapidamente, reduzir os custos de TI e dimensionar.

  Para saber mais, consulte:
  - [Nuvem da Amazon Web Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/amazon-web-services-cloud-platform.html);
  - [Armazenamento](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/storage-services.html);
  - [Serviços computacionais](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html);
  - [Redes e entrega de conteúdo](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/networking-services.html);
  - [Banco de dados](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/database.html);

- O AWS Support oferece vários planos que disponibilizam acesso a ferramentas e conhecimentos que respaldam o sucesso e a integridade operacional das suas soluções da AWS. Todos os planos de suporte fornecem acesso 24 horas por dia, 7 dias por semana, a atendimento ao cliente, documentação da AWS, documentos técnicos e fóruns de suporte. Para obter suporte técnico e mais recursos para planejar, implantar e melhorar ambientes da AWS, selecione o plano de suporte que melhor se alinhe aos vários casos de uso da AWS.

  Para saber mais, consulte:
  - [Conceitos básicos do AWS Support](https://docs.aws.amazon.com/awssupport/latest/user/getting-started.html)
  - [Compare planos do AWS Support](https://aws.amazon.com/premiumsupport/plans/)

### Fechamento
- Para começar, vamos ver os aspectos de Implantação e Operação da AWS
  - Imagine um grupo de componentes em que todos fazem parte de uma arquitetura maior. Você possui componentes como um balanceador de carga, alguns servidores web, servidores de aplicativos e seus bancos de dados de back-end.
  - Esta é uma configuração bastante típica mas existem várias coisas a se considerar. Estas são
    - **COMO:** Como você gerencia estes vários componentes?
      - O Console pode ser de alguma ajuda, mas dificulta muito a documentação dos processo com as atualizações de interface.
      - A automação de atividades se torna quase impossível;
      - Como lidar se você precisar realizar operações em vários servidores de uma só vez?
      - No Console, as operações que você pode distribuir são mínimas;
      - **Se você precisa gerenciar sua infraestrutura como um todo, a utilização do console pode ser um empecilho.**
      - Neste caso, pode-se utilizar os **SDKs** ou o **CLI** ou até mesmo o **AWS CloudFormation** ou outro serviço de IaC.
    - **ONDE:** Onde você vai construiur?
      - Onde estão meus usuários?
      - É preciso considerar algum regulamento sobre a soberania dos dados?
      - Armazenamento em cache vai melhorar a experiência dos usuários finais?
      - Como cuidar de alta disponibilidade e recuperação de desastres?
    - **O QUÊ?** Quais serviços e ferramentas você implementará?
      - Qual combinação de componentes ajudará você a atingir os objetivos estabelecidos?
      - Se você está migrando infraestrutra local, quais os requisitos do seu ambiente on-premises que você precisa atender e quais serviços podem ajudar nisso?
      - Pensando no caso anterior
        - Opção 1:uma solução poderia ser utilizar um banco autogerenciado em uma EC2. Neste caso, você terá acesso e controle total da instância, do mecanismo de banco de dados, configurações e poder completo sobre sua configuração do banco de dados. A desvantagem é que isso exigirá muito mais sobrecarga operacional. 
        - Opção 2: Utilizar serviços gerenciados como o RDS. VocÊ fica limitado em quais engines de banco você pode utilizar e não tem acesso root. Você tem muito controle mas não controle total.
        - 
