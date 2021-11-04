#AWS Cloud Practitioner Essentials (Second Edition)
Anotações sobre o treinamento da AWS dos serviços essenciais oferecidos por eles.

## Principais Serviços

### EC2 - Amazon Elastic Cloud Compute
Provê servidores de VM.

### EBS - Amazon Elastic Book Store
É um armazenamento de dados em HD ou SSD para uma instância do EC2. Ou seja, ao criar uma VM no EC2, os discos dela são os criados no EBS.

Um ponto importante é que as instâncias do EBS devem ser criadas na mesma zona/região (SP, NY, Tókio etc) da instância do EC2.

Comandos na VM:

```
SBLK
```
Mostra todos os discos do EBS vinculados na VM

```
MKE2FS
```
Criar um sistema de arquivo no disco (HDFS, DFS etc)

### S3 - Amazon Sample Storage Service
Utilizado para armazenar dados de diversos tipos e fontes, recomendado para trabalhar com Big Data.

- Buckets: local dentro da instância S3 para armazenar os dados/arquivos
- Objetos: são os arquivos dentro dos buckets, cada arquivo é um objeto.

### VPC - Amazon Virtual Private Cloud
Se comporta como se fosse uma VPN só que em um ambiente em nuvem.

### Load Balancer
Distribui ou redireciona o trafego das requisições conforme o conteúdo delas.

### Auto Scaling
Redimensiona as configurações de alguns serviços conforme necessidade. 

Por exemplo: é possível diminiur a memória RAM de uma VM (EC2) durante a noite ou aumentar quando tiver mais uso.

### Route S3
É um serviço para resolver DNS

### RDS
Serviços de banco de dados relacionais. É possível criar instâncias de BD SQL Server, Postgres, MySQL etc.

### AWS Lambda
Execução de códigos fonte para API, ETL, processamento de imagens etc.

### AWS Elastic Beanstalk
PaaS utilizado para gerenciamento de toda uma aplicação Web

### SNS - Sample Notification Service
Envia notificações via e-mail, apps baseados em eventos no serviço da AWS

### Amazon CloudWatch
É um serviço que monitora e recupera estatísticas/métricas de uso e logs dos serviços AWS.
Ele conta com um alarme que é possivel programar para ser disparado quando algum evento baseado no uso acontecer conforme programado.
Exemplo: se o uso de CPU de um serviço for maior de 60% por mais de 5 minutos, enviar uma notificação via o SNS ou chamar um evento no Auto Scaling para redimensionar o CPU

### Amazon CloudFront
Armazena conteúdo em cach em um servidor mais próximo da onde está sendo feito a requisição.
O conteúdo salvo em cach pode ser Web (arquivos estáticos) ou do tipo RTMP (arquivos de streamiing).
Um exemplo: tenho uma aplicação em um server em Seattle no Estados Unidos e acesso ela no Brasil. Se necessitar de que alguma requisição seja mais rápida, basta criar um serviço no CloudFront em São Paulo apontando como origem o o servidor em Seattle.



