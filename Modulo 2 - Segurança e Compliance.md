# Segurança e Compliance

- **Entender quem é responsável pelo o que em relação a segurança**
- Na nuvem, alguns aspectos técnicos sobre como os serviços são hospedados ou como os dados são armazenados podem ser abstraídos de você. **Porém, isto não significa que você não é responsável pela segurança na nuvem.**
- Você deve ser capaz de identificar quando medidas de segurança precisam ser aplicadas e quando elas já estão sendo cuidadas pela AWS.

### Modelo de Responsabilidade Compartilhada
- O Cliente é responsável pela segurança NA nuvem:
  - Seus dados;
  - Plataforma, aplicativos e gerenciamento de identidade e acesso;
  - Configurações de sistema operacional, rede e firewall;
  - Criptografia e autenticação da integraidade de dados do cliente
  - Criptografia do servidor e/ou sistema de arquivos;
  - Proteção do tráfego de redes (Criptografia, Integridade e Identidade)
- A AWS é responsável pela segurança DA nuvem:
  - Software:
    - Computação; Armazenamento; Bancos de Dados; Redes;
  - Hardware/Infra Global da AWS:
    - Regiões; Zonas de Disponibilidade; Locais de Borda;

  - Ser capaz de saber quando é necessário proteger recursos na AWS e o quanto você precisa estar envolvido na segurança, o que pode variar entre serviços.
  - Não é necessário saber os passos para aplicar estas ações mas precisa saber, de maneira geral, quais recursos de segurança existem e quando você é responsável por ativá-las
  - Ser capaz de descrever como a responsabilidade de um cliente muda dependendo do serviço que ele está utilizando:
    - Exemplo: Ao hospedar um banco de dados MySQL no Amazon RDS, quem é responsável por corrigir a engine do Banco de Dados na instancia RDS ou é a AWS responsável pela correção? Como essa relação muda se o banco estiver hospedado em uma EC2?
    - Como resposta, no caso do RDS, a AWS é responsável pelo patch de segurança, enquanto no caso da EC2, a responsabilidade é do cliente
  - **As relações de segurança na AWS dependem se um serviço é gerenciado ou não gerenciado.**
    - No caso acima, RDS é um serviço gerenciado, ou seja, você precisa realizar menos atividades relacionadas a segurança e gerenciamento;
    - Por outro lado, EC2 é não gerenciado, significando que você tem mais controle sobre o serviço e com isso, mais responsável pela realização de tarefas de segurança e gerenciamento.
  - É importante saber a relação de responsabilidades **Cliente X AWS** para serviços como Amazon RDS, Amazon EC2, Amazon DynamoDB, Amazon Lambda entre outros.

#### Question Walkthrough
**Pergunta:** Qual das opções a seguir é **responsabilidade do cliente** segundo o modelo de responsabilidade compartilhada da AWS?
- A) Aplicação de patches na infraestrutura subjacente; *- Relacionado com a infraestrutura que hospeda os serviços AWS, ou seja, responsabilidade da AWS;*
- B) Segurança Física; *- Responsabilidade da AWS, relacionado com a infraestrutura Global.*
- **C) Aplicação de patches nas instâncias do Amazon EC2;**
- D) Aplicação de patches na infraestrutura de rede. *- Relacionado com a infraestrutura que hospeda os serviços AWS, ou seja, responsabilidade da AWS;*

### Conceitos de Segurança e Compliance
- Mesmo que você não seja a pessoa responsável pela criação da arquitetura, você deve ser capaz de encontrar as informações sobre segurança e compliance e **e quais serviços existem para dar suporte a um plano de segurança e compliance.**

- Defina os conceitos de segurança e compliance da AWS Cloud.
  - Onde encontrar informação:
    - Exemplo: Você está criando uma solução na AWS e esta precisa estar em conformidade com a LGPD e você deseja armazenar os dados no Amazon DynamoDB. Como saber se o DynamoDB está em conformidade com a LGPD.
    - Esta informaçao está no AWS Artifact: O qual dá acesso, sob demanda, a relatórios de segurança e compliance da AWS.
- Cada serviço da AWS tem diferença em relação a Compliance. Um serviço pode exigir que um conjunto de ações seja tomada para estar em conformidade, enquanto outro serviço pode exigir um conjunto diferente de ações a serem tomadas.
- **Para este exame, não é necessário saber exatamente quais são as ações necesárias a serem tomdas** mas sim saber onde encontrar as quais ações precisam ser tomadas e saber que estas ações variam de serviços para serviço.
- Além de saber onde encontrar informações sobre segurança e compliance, **você também precisa estar preparado para responder perguntar relacionadas às diferentes maneiras que segurança e compliance podem ser obtidas na AWS.**
- Quando pensar em segurança e compliance, a principal coisa que precisa estar em mente é tentar proteger sistemas e informações.
  - Uma das maneiras de fazer isto é através de criptografia.
    - Exemplo: Existe a criptografia de dados em trânsito (Enquanto ela se move entre dois locais) e a de dados em repouso (Dados armazenados).
  - Ser capaz de identificar quem ativa a criptografia para diferentes serviços da AWS, o que está relacionado com o modelo de responsabilidade compartilhada da AWS.
- Estar apto a identificar serviços que permitem registrar, auditar e criar relatórios sobre a atividade que acontecem na sua conta AWS.
  - Atividade em uma conta AWS pode ser um usuário da AWS criando ou modificando recursos ou usuários externos utilizando seus recursos.
- **Entenda o que são os logs e como utilizá-los para solicionar problemas ou auditar a atividade de uma conta da AWS.**
- Estar apto para distinguir entre serviços da AWS como:
  - AWS CloudWatch: Monitoramento e Observabilidade;
  - AWS CloudTrail: Registro da atividade da conta;
  - AWS Config: Auditoria e inventário de configuração.
- Nem toda pessoa utilizando uma conta AWS deve ter o mesmo nível de permissão. Ao invés disso, você deve seguir o conceito de **acesso mínimo**, no qual você concede às pessoas exatamente o nível de acesso que elas precisam.

#### Question Walkthrough
**Pergunta:** Qual o serviço que auxilia na **auditoria** de risco com o **monitoramento e o registro contínuos** da atividade da conta, incluindo as ações dos usuários no AWS management console e no SDK da AWS?
- A) AWS CloudWatch; *CloudWatch é um serviço para o monitoramento de dados gerados por recursos e visualizá-los como estatística em dashboards. Ele pode trazer insights sobre o estado de seus recursos e soluções na AWS.* Apesar de monitorar seus recursos, ele não permite nenhum tipode auditoria de risco. Ele pode fornecer informações se você tem uma instância EC2 sobrecarregada ou se você tem um número alto de requisições sendo recebida por um Elastic Load Balancer. Porém, não te permite monitorar chamadas de API feitas na sua conta.
- **B) AWS CloudTrail;**
- C) AWS Config; *É um serviço que permite avaliar, analisar e auditar as configurações dos recursos da AWS.* Ele monitora e regista continuamente suas configurações de recursos da AWS e permite automatizar a avaliação das configurações registradas em relação às configurações desejadas.
- D) AWS Health; *É um serviço que mostra continuamente a disponiblidade dos recursos da AWS que você utiliza.*

- **OBS:** Ações na AWS são realizadas através de chamadas de API e cada chamada de API é capturada através do serviço AWS CloudTrail
  - Isto inclui quem criou a chamada, qual era a chamada e a resposta daquela chamada.

### Recursos de gerenciamento de acesso da AWS
- **Identificar os recursos de gerenciamento de acesso da AWS.**
- Entender a necessidade de gerenciamento de usuário e identidade. **Porque você precisa de ferramentas para controlar o acesso do usuário?**
  - Nem todos que usam uma conta AWS precisam do mesmo nível de acesso. Para controlar como as pessoas usam os serviços da AWS dentro de uma conta, se faz necessário existir uma maneira de controlar o nível de acesso que elas têm.
- Estar familiarizado com o conceito de **Menor privilégio necessário.**.
- Tudo isto é feito pelo serviço **AWS Identity and Access Management (IAM)**.
- Ao criar uma conta AWS, você começa com uma identidade de autenticação que tem acesso completo a todos os recursos e serviços da AWS na conta: essa identidade é chamada **Usuário Root** da conta AWS.
- Para o exame, é necessário ser capaz de explicar que o usuário root é diferente dos outros tipos de usuários de uma dada conta AWS.
  - O usuário root tem acesso completo e irrestrito a todos os recursos em uma conta AWS e **você não deve utilizar este usuário para realizar tarefas diárias na AWS.**
- Para proteger o usuário root, é necessário tomar certas ações como: autenticação multi-fator (MFA), bloquear as credenciais, rotacionar access keys e senhas e não utilizá-lo.
- Existe um número limitado de tarefas que exigem a utilização do usuário root e é necessário estar familiariazado com estas tarefas.

- Entender quais recursos o IAM possui e quando utilizá-los.
  - Usuários;
    - Ser capaz de explicar que usuários possuem usuários e senhas associados à eles; Possuem chave de acesso para acesso programático; Usuários podem ter o MFA ativado para utilizar a console; Como é possível impor complexidade às suas senhas e rotacionamento de chaves de acesso e senhas.
  - Grupos;
    - Como organizar usuários em grupos e como isso afeta as permissões quando ações da AWS são tomadas.
  - Perfis (Roles);
    - São credenciais temporárias que podem ser assumidas por diversas entidade e possuem diversas utilizações.
      - Exemplo de utilização:
        - Um usuário pode assumir uma role para obter acesso temporário a permissões;
        - Um programa pode assumir uma role para obter acesso à credenciais da AWS para fazer chamas de API da AWS;
        - Pode-se utilizar roles para acesso entre contas (CrossAccount).
  - Políticas (Policies)
    - Existem diferentes tipos de policies:
      - Politicas gerenciadas:
        - Criadas e editadas pela AWS;
      - Politicas não gerenciadas:
        - Criadas e editadas pelo usuário;
  Saber como permissões na AWS funcionam em uma visão mais geral, ou seja, como aplicar politicas do IAM a usuários, grupos ou perfis e o impacto que isso tem no acesso de uma dada entidade.
- **Você pode utilizar politicas do IAM para controlar ao que os usuários da AWS têm acesso, definindo quais chamas de API os usuários têm permissão para fazer.**

#### Question Walkthrough
**Pergunta:** Qual destes itens pode limitar o acesso de buckets do **Amazon Simple Storage Service (Amazon S3)** a determinados usuários?
**Respostas:**
- A) Pares de chaves públicas e privadas; - *Acesso a um bucket do S3 é controlado por meio da política do bucket e das políticas do IAM aplicadas às identidade que tentam acessar o S3.*
- B) Amazon Inspector; - *É um serviço que executa avaliações de segurança em instâncias do EC2*
- **C) Políticas do AWS Identity and Access Management (IAM);**
- D) Grupos de Segurança - *Security Groups são firewalls no nível da instância EC2.*

### Recursos para o suporte de segurança

- Identificar recursos par ao suporte de segurança.
- É importante entender que caso você não seja um profissional de segurança, você não será a pessoa responsável por construir soluções de segurança, **mas será a pessoa que orientará as pessoas com relação às soluções que atendam às necessidades delas.**. Para fazê-lo, você precisa saber quais serviços existem para isto e onde encontrar informações sobre os mesmos.

- No que diz respeito a segurança de rede, você precisa estar apto a responder questões sobre a funcionalidade básica para serviços de segurança na AWS como:
  - Grupos de Segurança (Security Groups);
  - Listas de controle de acesso à rede;
  - AWS Web Application Firewall (WAF).
Não é necessários saber as funcionalidades de cada um deles mas saber quando usá-los e quais as suas funções.

- É imporante estar ciente que existem serviços como AWS Trusted Advisor e Amazon Inspector, que podem fornecer recomendações sobre segurança.
- Ainda, é importante saber que em alguns casos, a solução para seus problemas de segurança e compliance pode estar em ferramentas terceiras. Estas ferramentas podem ser encontradas na **AWS Marketplace**. É importante entender a diferença entre ferramentas e softwares encontrados no Marketplace versus soluções nativas da AWS.

- Ser capaz de utilizar o **AWS Knowledge Center** para encontrar mais informações e respostas para perguntas mais profundas, assim como no **Security Center, blogs e fórum de segurança da AWS.**

#### Question Walkthrough
**Pergunta:** Qual serviço ou recurso da AWS pode ser usado para **impedir ataques de injeção SQL**?
**Respostas:**
- A) Security Groups; - *São firewalls no nível de instâncias EC2. Security Groups permitem tráfego na EC2 com base em Portas, Protocolos e Origem/Destino. Eles não são capazes de inspecionar um pacote HTTP.*
- B) ACLs de rede; - *Os ACLs de rede controlam o tráfego com base no tipo do tráfego, porta, protoclo, origem/destino.*
- **C) AWS WAF;** - *É um firewall que pode filtrar tráfego com base em qualquer parte da solicitação, como endereços IP, cabeçalhos HTTP, corpo HTTP ou strings URI.*
- D) Políticas do IAM - *Policies são anexadas às entidades da AWS, como usuários, grupos ou perfis do IAM, definindo quais ações podem ou não ser tomadas.*

- **Security Groups x ACLs:** Security Groups são firewall no nível de instâncias EC2 enquanto ACLs são firewalls no nível de SubRede.


### Domain Notes

- Leia o whitepaper [Introdução à segurança da AWS](https://docs.aws.amazon.com/whitepapers/latest/introduction-aws-security/welcome.html).

- Saiba mais sobre o [Modelo de responsabilidade compartilhada da AWS](https://aws.amazon.com/compliance/shared-responsibility-model/).

- O AWS Artifact é sua primeira opção de recurso para informações relacionadas à conformidade que importam para você. Ele oferece acesso sob demanda aos relatórios de segurança e conformidade da AWS e a contratos on-line específicos. Saiba mais sobre o [AWS Artifact](https://aws.amazon.com/artifact/).
  
- Leia o whitepaper [Amazon Web Services: risco e conformidade](https://docs.aws.amazon.com/whitepapers/latest/aws-risk-and-compliance/welcome.html).

- Saiba mais sobre os [Programas de conformidade da AWS](https://aws.amazon.com/compliance/programs/).

- Saiba mais sobre os [Serviços de segurança da AWS](https://aws.amazon.com/products/security/?nc=sn&loc=2).

- Saiba mais sobre o [AWS Identity and Access Management (IAM)](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html).

- Saiba mais sobre o [princípio de menor privilégio](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege).

- Saiba mais sobre o [Usuário-raiz da conta da AWS](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html).

- Saiba mais sobre a [autenticação multifator (MFA) do usuário-raiz da conta no IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html#id_root-user_manage_mfa).

- Saiba mais sobre as [tarefas que exigem o acesso do usuário-raiz à conta](https://docs.aws.amazon.com/general/latest/gr/root-vs-iam.html#aws_tasks-that-require-root).

- Saiba mais sobre o [AWS CloudTrail](https://aws.amazon.com/cloudtrail/).
- 
- Saiba mais sobre o [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/).

- Saiba mais sobre o [AWS Config](https://aws.amazon.com/config/).

- Explore a [central de conhecimento da AWS](https://aws.amazon.com/premiumsupport/knowledge-center/).

- Explore a [Central de Segurança da AWS](https://aws.amazon.com/security/).

- Explore os [fóruns de discussão de segurança da AWS](https://repost.aws/tags/TAearVnHruTomUO6FRBaV35A?origin=forums). (Observação: exige que você inicie a sessão na conta da AWS.)

- Explore o [Blog de segurança da AWS](https://aws.amazon.com/blogs/security/).

- Saiba mais sobre as [listas de controle de acesso (ACLs de rede) na AWS](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html).

- Saiba mais sobre [grupos de segurança](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html).

- Saiba mais sobre as [práticas recomendadas de segurança para nuvens privadas virtuais (VPCs)](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-security-best-practices.html).

### Fechamento
- Segurança e Compliance são chamados de **TRABALHO ZERO**** na AWS. Isto significa que segurança e compliance são mais importantes do que qualquer outra prioridade.
- Para evitar violações de segurança, você deve saber como a segurança é abordada dentro da AWS e quais ferramentas e serviços existem para dar suporte a um plano de segurança e compliance.

- **Exemplo:** Saber que o modelo de responsabilidade compartilhada define quem é responsável pelo que na AWS. A partir destas ideias, que são apenas diretrizes, é necessário entendê-las e colocá-las em prática.
  - Entender que seus dados pertencem a você na AWS, você precisa saber quais os programas de compliance você precisa aderir para proteger esses dados. Isto inclui criptografia, como assegurar a criptografia de dados ociosos e em trânsito;
  - Entender quais tipos de técnias de criptografias podem ser aplicadas e quais serviços da AWS oferecem ferramentas ou recursos de criptografia podem te ajudar a implementar uma boa prática de segurança ao usar a AWS;
  - **Exemplo Prático:** Sua empresa está em busca de uma solução para armazenamento de daos que atenda às necessidades de compliance e você está ajudando a tomar as decisões de design.
    - Um ótimo serviço de armazenamento é o Amazon S3;
    - Saber que no S3 você pode ativar criptografia no nível do Bucket pode ajudar a fazer recomendações de design que atendam às normas de conformidade
  - **Ao invés de construir soluções do zero, você pode simplesmente usar os recursos e serviços integrados na AWS.** 
- Como parte do exame, você precisa saber quais serviços da AWs existem para identificar e auditar eventos relacionados à segurança, como:
  - AWS CloudWatch;
  - AWS CloudTrail;
  - AWS Config;
  - AWS Inspector;
  - Entre Outros...
- **O motivo para conhecer estes recursos é que geralmente os incidentes relacionados à segurança não são totalmente óbvios. Para identificar os eventos relacionados à segurança, você precisa ter visibilidade sobre seus recursos da AWS, além de poder ver o histórico de eventos que ocorream em sua conta AWS.**
- **Exemplo:** Digamos que alguém está repetidamente assumir uma role para obter acesso à credenciais. Como saber se isso está acontecendo em sua conta?
  - Se você não souber onde procurar, pode ser difícil buscar por informações. Porém *se você souber, dê uma olhada nos logs do CloudTrail*, onde esse tipo de atividade de API da AWS é capturado.