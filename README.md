# Book Gateway

Este é o gateway para o projeto Book API. Ele roteia as solicitações para os microserviços apropriados.

## Instalação

### Pré-requisitos

- [Java 17+](https://adoptopenjdk.net/)
- [Gradle](https://gradle.org/)
- [Docker](https://www.docker.com/)

### Passos para Instalação

#### Método 1: Usando Java

1. Clone o repositório do gateway:
    ```sh
    git clone https://github.com/seu-usuario/book-gateway.git
    cd book-gateway
    ```

2. Compile o gateway:
    ```sh
    ./gradlew build
    ```

3. Execute o gateway:
    ```sh
    ./gradlew bootRun
    ```

#### Método 2: Usando Docker

1. Certifique-se de que a rede Docker foi criada:
    ```sh
    docker network create book-network
    ```

2. Construa a imagem Docker da Book Gateway:
    ```sh
    docker build --tag book-gateway .
    ```

3. Rode o contêiner da Book Gateway:
    ```sh
    docker run --name book-gateway --network book-network book-gateway
    ```

Certifique-se de configurar corretamente o arquivo de propriedades antes de iniciar o gateway.

## Configuração

O gateway pode ser configurado por meio do arquivo `application.properties`. Certifique-se de ajustar as configurações conforme necessário para o seu ambiente.

Exemplo de arquivo de propriedades:

```properties
spring.application.name=book-gateway
server.port=8080

# Eureka
eureka.client.service-url.defaultZone=http://localhost:8761/eureka
```

Certifique-se de ter os microserviços apropriados em execução para que o gateway possa rotear as solicitações corretamente.

Fique à vontade para contribuir com este projeto.
