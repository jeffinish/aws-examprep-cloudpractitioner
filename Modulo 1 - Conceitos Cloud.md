# Cloud concepts

## Tópicos de conceitos da AWS Cloud
### Defina o que é a AWS Cloud e qual a proposta de valor dela;
- Definir a AWS Cloud: Explicar os beneficios da AWS Cloud em várias áreas;
  - Em relação a segurança, o que a a AWS pode oferecer?
    - Automatização de ações baseada em eventos de segurança;
    - Restrição de acesso a usuários;
  - Em relação a alta disponibilidade, o que a AWS pode oferecer?
    - Zonas de Disponibilidade, Regiões e Elastic Load Balancing ajudam a construir ambientes escaláveis;
    - Definições de preço *as you go*.
  - Utilizando a AWS, pode-se mover pessoas do gerenciamento de infra-estrutura local (OnPremise) como Aquisição, manutenção e gerencial de servidores e/ou outros aspectos relacionados ao funcionamento de um DataCenter, levando-os a priorizar outras atividades tais como: otimização de recursos, melhoria de software, melhor experiência do cliente final entre outras que podem ajudar a operação da empresa ser mais eficiente.

#### Question Walkthrough
- Como lidar com as questões do exame:
  - Leia a Pergunta;
  - Identifique as principais palavras e frases;
  - Leia as respostas;
  - Identifique a resposta correta;

**Pergunta:** *A possibilidade de dimensionar horizontalmente as instâncias do Amazon EC2 sob demanda* é um exemplo de qual **conceito na proposta de valor da AWS Cloud**?
**Respostas:**
- A) Economia de dimensionamento - Está relacionado à capacidade da AWS de compra em larga escala, com preços reduzidos e assim, podendo oferecer melhores preços para seus clientes;
- **B) Elasticidade**
- C) Alta Disponibilidade - Está relacionado com evitar pontos únicos de falha na arquitetura;
- D) Agilidade - Está relacionado com a habilidade de remover ou incluir nos recursos ou recursos já existentes na sua arquitetura.

### Identifique as proposta de valor da AWS Cloud;
- Aspectos economicos da AWS Cloud: como a operação na AWS afeta os custos operacionais e de propriedade da organização
- Conceitos de custo total de propriedade (TCO):
  - Despesas Operacionais (OpEx);
    - Custos diários da organização, como serviços e itens que são utilizados. Como por exemplo: Tonner, host web e outras coisas necessárias para a operação da empresa.
    - **Não são investimentos a longo prazo, mas sim custos pra continuar em operação**
  - Despesas de capital (CapEx);
    - Custos associado à criação dos beneficios de longo prazo. Como por exemplo: compra de um prédio, servidores;
    - São geralmente comprados apenas uma vez e espera-se que estes auxiliem a empresa por anos.
  - Custos de mão de obra associados a operação On-Premises;
    - Auto explicativo. Como exemplo, temos os técnicos de rede que lidam com a instalação, configuração dos servidores e infraestrutura.
    - Eles são pagos pelo serviço deles e este serviço é necessário para manter a infraestrutura on-premises.
  - Impacto do custo de licenciamento de software
    - O movimento para a nuvem pode gerar transtorno quando tratamos de licenciamento de software. Alguns casos, a migração pode ocorrer sem problemas, em outros, são exigidos outro tipo de licença ou ainda, pode-se abrir mão das licenças já obtidas em fator das gerenciadas pela própria AWS.

- Identificar quais operações vão reduzir custos ao serem migradas para a nuvem;
  - Normalmente, a migração para a nuvem não é uma tradução 1-1. Apesar de alguns aplicativos poderem ser migrados diretamente, geralmente existem outras coisas que precisam ser consideradas por serem mais econômicas;
  - **Parte disso é determinar exatamente o que é necessário, por meio de comparação e teste de desempenho. Em vez de focar o provisionamento de recursos para os picos de demanda, pode-se avaliar o que é necessário e buscar outras maneiras de atender este pico de demanda.**
  - Uma maneira de lidar com isso, pode ser configurar uma automação, como scaling automatizado de recurso pode atender as necessidades. Com isso, não se faz necessário utilizar atender suas necessidades sem utilizar a capacidade projetada para o pico de utilização quando não estiver com pico de demanda.
  - O uso de serviços gerenciados pode ajudar a reduzir sua carga de trabalho técnica e os custos para uma variedade de áreas.

- Operações de redução de custos
  - Dimensionamento correto de infraestrutura;
  - Automação;
  - Redução do escopo de conformidade;
  - Serviços gerenciados;

#### Question Walkthrough
- **Mesmo que a pergunta não deixe claro, a pergunta sempre está buscando A MELHOR resposta possível.** Por exemplo, existe a possiblidade de que varias respostas sejam verdadeiras, mas uma será a melhor resposta possível.


**Pergunta:** *Qual despesa on-premises será reduzida se a empresa* **migrar o aplicativo para o Amazon EC2**?
- **A) Custos do hardware do servidor;**
- B) Custos do armazenamento no Amazon EBS - É um custo que pode não ter sido considerado ao executar os processos on-premises.
- C) Custos de backup do armazenamento - Custos de Backup não estão associados ao custo da EC2;
- D) Custo da transferência de dados para fora da internet - Custos de transferência de dados não estão associados ao custo da EC2.

#### Explique os princípios do projeto de arquitetura da nuvem.
- Ser capaz de entender e explicar os principais principios de design que são referenciados em diversas boas práticas e arquiteturas recomendadas. Estes são:
  - **Design à prova de falhas**;
    - Entenda como e quais componentes podem falhar e como arquitetar falhas para adicionar resiliência.
    - Um exemplo: Uma aplicação que pode rodar em apenas um servidor mas usando pelo menos dois servidores. Neste caso, estaríamos projetando a arquitetura levando em consideração a falha do seu servidor.
  - **Componentes desacoplados versus arquitetura monolítica**;
    - Arquiteturas monolíticas se referem a quando todos os processos são fortemente acoplados ou conectados e são executados como um único serviço.
    - Um problema que pode surgir com esse design é: Se um processo do aplicativo apresentar um pico de demanda, a arquitetura inteira deverá ser dimensionada.
    - Além disso, aprimorar e atualizar aplicativos monolíticos pode ser mais complexo devido ao alto nível de interconectividade;
    - O outro lado disso, seria o desacoplamento dos componentes da arquitetura.
    - Um exemplo: Se a aplicação que consideramos acima, estiver utilizando um banco de dados e este está no mesmo servidor que o restante dos componentes, é provável ocorrer um evento onde os níveis de utilização dos componentes do aplicativo e do banco de dados estão em níveis distintos. Além disso, atualizações em um dos serviços pode significar tempo offline para ambos e o mesmo acontece no caso de falha, pode impactar ambos.
    - Se desacoplar cada aplicação do banco de dados, você seria capaz de dimensionar e gerenciar cada um baseado na sua própria necessidade. Além disso, a falha de um dos componentes, não implicaria diretamente na falha do banco de dados.
  - **Implementando elasticidade na nuvem Versus on-premises**;
    - Continando com o exemplo que estamos utilizando, se a demanda aumenta depois que a infraestrura foi implantada, gerenciar essa demanda adicional é muito dificil. Além disso, se houver menos demanda, sua capacidade não utilizada se torna desperdício de dinheiro.
    - Na AWS você tem a possiblidade de mudar dinamicamente sua capacidade baseado na sua demanda. Precisando de 2, 200 ou 2000 servidores, é possivel escalar estes números para atender sua demanda e ainda diminuir estes números quando não precisar mais.
  - **Pense Paralelo**
    - Dependencias podem criar ou quebrar processos inteiros e qualquer falha na pipeline significa uma falha no processo como um todo.
    - *Pensar Paralelo* é semelhante ao desacoplamento mas você está pensando em como é possível dividir um trabalho de forma mais simples e então, distribuir esta carga de trabalho para varios componentes para lidar com processamento.
    - Ainda utilizando o exemplo da aplicação superior: Se os servidores estão processando todas as solicitações sequencialmente e estão recebendo muitas requisições, eles conseguiram lidar com apenas um número limitado dessas solicitações. Se algo acontecer, não será uma falha, mas um dos servidores ficar dependente do processamento do anterior e assim, todas as próximas requisições estarão em espera, ou ainda pior, elas podem ser recusadas até o processamento se reestabelecer.
    O que pode ser feito para resolver isso, é ter um elemento, como um *Load Balancer* para receber as requisições e distribuir para os servidores e assim, cada um poderá processar na sua velocidade mas sem atrasar o restante das requisições.

#### Question Walkthrough
**Pergunta:** Qual das opções representa um principio de projeto de arquitetura da AWS Cloud?
**Respostas:**
- A) Implementar pontos únicos de falha; - O oposto de evitar pontos únicos de falha;
- **B) Implementar acoplamento fraco**;
- C) Implementar projeto monolítico; - O oposto de desacoplar e evitar designs monolíticos;
- D) Implementar scaling vertical; - O principio indica implementar scaling HORIZONTAL.

### Domain Notes
- Esta credencial ajuda as organizações a identificar e desenvolver talentos com habilidades críticas para a implementação de iniciativas na nuvem. Obter a certificação AWS Certified Cloud Practitioner valida a fluência na nuvem e o conhecimento fundamental sobre a Amazon Web Services (AWS).

  Saiba mais em: [AWS Certified Cloud Practitioner](https://aws.amazon.com/pt/certification/certified-cloud-practitioner/)

- Para obter essa certificação, você precisará fazer e ser aprovado no exame AWS Certified Cloud Practitioner. Esse exame tem uma combinação de dois formatos de pergunta: múltipla escolha e múltipla resposta. Há outras informações, como esboço do conteúdo do exame, neste guia do exame.

  Saiba mais no: [Guia do exame AWS Certified Cloud Practitioner](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf)

- A computação em nuvem oferece uma forma simples de acessar servidores, armazenamento, bancos de dados e um conjunto amplo de serviços de aplicativos pela Internet. Um provedor de serviços de nuvem, como a AWS, é proprietário e faz a manutenção do hardware conectado à rede necessário para esses serviços de aplicativos, enquanto você provisiona e utiliza o que precisa por meio de um aplicativo web. Esse estilo de computação oferece muitos benefícios que podem ajudar o seu negócio.

  Saiba mais em: [Seis vantagens da computação em nuvem](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

- No início, a AWS pode parecer complicada. A criação de infraestruturas de modo nativo na nuvem pode ser muito diferente da tradicional criação on-premises. E, independentemente de ser seu primeiro trabalho com infraestrutura ou de você ter usado o kernel Linux na última década, pode ser difícil saber por onde começar.

  Saiba mais em: [Fundamentos da AWS: principais conceitos](https://aws.amazon.com/pt/getting-started/cloud-essentials/)

- O AWS Cloud Economics desenvolveu a Cloud Value Framework para ajudar as organizações a elaborar casos de negócio abrangentes para a nuvem, avaliando e acompanhando o progresso em relação a quatro dimensões de valor importantes: economia de custos, produtividade das equipes, resiliência operacional e agilidade empresarial. Este artigo mostra como a nuvem AWS está transformando negócios e fornece uma análise desses quatro aspectos do valor comercial.

  Saiba mais em: [Valor comercial na AWS](https://aws.amazon.com/pt/executive-insights/content/business-value-on-aws/)

- A AWS fornece algumas ferramentas voltadas para avaliação de preço e custo. Caso os detalhes e serviços da carga de trabalho a serem usados sejam identificados, a calculadora de preço da AWS pode ajudar a calcular o custo total de propriedade. O Migration Evaluator ajuda você a inventariar seu ambiente existente, identificar informações de carga de trabalho e projetar e planejar sua migração para a AWS.

  Saiba mais em: [Ferramentas de custo total de propriedade/preços da AWS](https://docs.aws.amazon.com/whitepapers/latest/how-aws-pricing-works/aws-pricingtco-tools.html)

- Definir o tamanho certo é o processo de corresponder os tipos e tamanhos de instâncias com os requisitos de desempenho e capacidade de carga de trabalho, com o menor custo possível. É também o processo de examinar as instâncias implantadas e identificar oportunidades para removê-las ou reduzi-las sem comprometer a capacidade ou outros requisitos, o que resulta em custos mais baixos.

  Saiba mais em: [Otimização do seu custo com as recomendações de definição do tamanho certo](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-rightsizing.html)

- O AWS Well-Architected ajuda arquitetos de nuvem a criar infraestruturas seguras, resilientes, eficientes e de alto desempenho para aplicativos e cargas de trabalho. Baseado em cinco pilares (excelência operacional, segurança, confiabilidade, eficiência de desempenho e otimização de custos), ele fornece uma abordagem consistente para que clientes e parceiros da AWS avaliem arquiteturas e implementem designs que podem ser dimensionados com o tempo.opp

  Saiba mais em: [AWS Well-Architected](https://aws.amazon.com/pt/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc&wa-guidance-whitepapers.sort-by=item.additionalFields.sortDate&wa-guidance-whitepapers.sort-order=desc)

- Ao projetar soluções de tecnologia na AWS, se você ignorar os cinco pilares (excelência operacional, segurança, confiabilidade, eficiência de desempenho e otimização de custos), poderá ser desafiador criar um sistema que atenda às suas expectativas e requisitos. Incorporar esses pilares em sua arquitetura ajuda a produzir sistemas estáveis e eficientes. Isso permite que você se concentre em outros aspectos do design, como os requisitos funcionais.

  Saiba mais em: [Os cinco pilares do AWS Well-Architected Framework](https://aws.amazon.com/pt/blogs/apn/the-6-pillars-of-the-aws-well-architected-framework/)

### Fechamento