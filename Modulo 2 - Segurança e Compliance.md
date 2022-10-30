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
