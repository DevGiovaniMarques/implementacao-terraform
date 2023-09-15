# implementacao-terraform
Implementação de um conjunto de instâncias EC2 utilizando o Terraform e configuração do AWS Systems Manager fazendo uso do Amazon Simple Notification Service para instalação automatizada de agentes de segurança

Nesse projeto baseado em um cenário do mundo real, atuei como Engenheiro de DevSecOps, onde implementei um conjunto de instâncias EC2 e a infraestrutura de forma automatizada utilizando Terraform (infraestrutura como código — IaC). Além disso, foi necessário instalar um agente de segurança específico e de forma automatizada em todas as instâncias.

Uma vez que provisionei a infraestrutura, foi utilizado o AWS System Manager e seu componente Command Run para a instalação dos agentes de segurança de forma automatizada. Fiz uso do Amazon Simple Notification Service — SNS para enviar um e-mail informando que todo o processo foi concluído com sucesso.

![alt text](PORTFOLIOPROJETO_AWSMODULO5_ARQUITETURA-220624-162245.png)

Primeiro passo do projeto foi fazer o download dos arquivos que usei para criar as instâncias pelo Terraform, abri os arquivos no VsCode para editá-los, e colocar as informações do seu ambiente na AWS.

Após isso abri o Aws CloudShell para importar os arquivos e instalar o Terraform, para executar os comandos e criar as duas instâncias EC2.

Depois de instalado foi só executar os comandos:

```
terraform init
terraform plan
terraform apply
```

Com isso as duas instâncias EC2 foram criadas.

![alt text](https://github.com/DevGiovaniMarques/implementacao-terraform/blob/b601d9c62c6ed2b4039e5fd0f60c7dad63f46a64/2023-07-01%2020_30_18-Instances%20_%20EC2%20Management%20Console%20e%20mais%2015%20p%C3%A1ginas%20-%20Pessoa%201%20%E2%80%94%20Microsoft%E2%80%8B%20Edg.png)

Depois criei uma notificação no Amazon Simple Notification Service — SNS

![alt text](https://github.com/DevGiovaniMarques/implementacao-terraform/blob/b601d9c62c6ed2b4039e5fd0f60c7dad63f46a64/2023-07-01%2020_30_56-Topics%20_%20Amazon%20SNS%20e%20mais%2015%20p%C3%A1ginas%20-%20Pessoa%201%20%E2%80%94%20Microsoft%E2%80%8B%20Edge.png)

Após a notificação criada, foi necessário fazer as configurações no AWS System Manager para realizar as instalações dos agentes de segurança de forma automática.

![alt text](https://github.com/DevGiovaniMarques/implementacao-terraform/blob/b601d9c62c6ed2b4039e5fd0f60c7dad63f46a64/2023-07-01%2020_31_41-AWS%20Systems%20Manager%20-%20QuickSetup%20e%20mais%2015%20p%C3%A1ginas%20-%20Pessoa%201%20%E2%80%94%20Microsoft%E2%80%8B%20Edge.png)

Com isso finalizamos as configurações necessárias e cada evento que acontecer nas instâncias EC2, será notificado via e-mail.

![alt text](https://github.com/DevGiovaniMarques/implementacao-terraform/blob/b601d9c62c6ed2b4039e5fd0f60c7dad63f46a64/2023-07-02%2000_17_37-Email%20%E2%80%93%20Giovani%20Marques%20Garrucho%20%E2%80%93%20Outlook%20e%20mais%2013%20p%C3%A1ginas%20-%20Pessoa%201%20%E2%80%94%20Micros.png)

Esse projeto foi bastante interessante de trabalhar, pois te dá uma visão totalmente diferente de como você pode provisionar recursos de forma simples e de alta escala de forma simples e rápida.



