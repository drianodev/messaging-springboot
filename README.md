# Messaging Spring Boot Project

Este projeto tem como objetivo proporcionar uma experiência de aprendizado sobre mensageria utilizando o framework Spring e o Apache Kafka.

## Requisitos

Certifique-se de ter o [Docker](https://www.docker.com/) instalado em seu ambiente.

## Instruções de Uso

### 1. Inicializando o Kafka e o Zookeeper

O projeto utiliza o Docker para simplificar a configuração do Apache Kafka e o Zookeeper. Execute o seguinte comando na raiz do projeto:

```bash
docker-compose up
```

Este comando iniciará os serviços do Zookeeper e Kafka em containers Docker.

### 2. Iniciando a Aplicação Spring Boot

A aplicação Spring Boot está configurada para se comunicar com o Kafka.

A aplicação estará disponível em [http://localhost:8080](http://localhost:8080).

### 3. Enviando Mensagens

Você pode enviar mensagens para o Kafka acessando a seguinte URL:

```bash
curl http://localhost:8080/kafka/hello/{name}
```

Substitua `{name}` pelo nome desejado. A mensagem será enviada para o tópico "hello-topic" no Kafka.

### 4. Consumindo Mensagens

A aplicação Spring Boot possui um consumidor de exemplo que imprime as mensagens recebidas. Confira o console para ver as mensagens de log.

## Estrutura do Projeto

### 1. `HelloController`

Um controlador simples que permite o envio de mensagens para o Kafka.

### 2. `HelloProducer`

Um produtor de mensagens Kafka que envia mensagens para o tópico "hello-topic".

### 3. `HelloConsumer`

Um consumidor de mensagens Kafka que escuta o tópico "hello-topic" e imprime as mensagens recebidas.

## Observações

Este projeto é uma iniciativa de aprendizado sobre mensageria utilizando o Spring e o Kafka. Sinta-se à vontade para explorar, modificar e experimentar com diferentes aspectos da integração entre Spring Boot e Apache Kafka.
