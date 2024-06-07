# Book Gateway

Este é o gateway para o projeto Book API. Ele roteia as solicitações para os microserviços apropriados.

## Instalação

### Pré-requisitos

- [Java 17+](https://adoptopenjdk.net/)
- [Gradle](https://gradle.org/)

### Passos para Instalação

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

Certifique-se de configurar corretamente o arquivo de propriedades antes de iniciar o gateway.

## Configuração

O gateway pode ser configurado por meio do arquivo `application.properties` ou `application.yml`. Certifique-se de ajustar as configurações conforme necessário para o seu ambiente.

Exemplo de arquivo de propriedades:

```properties
spring.application.name=book-gateway
server.port=8080

# Eureka
eureka.client.service-url.defaultZone=http://localhost:8761/eureka

## Uso

O gateway roteia as solicitações para os microserviços apropriados com base nos caminhos especificados.

### Endpoints Disponíveis

- `POST /api/books`: Cria um novo livro.
- `PUT /api/books/{id}`: Atualiza um livro.
- `DELETE /api/books/{id}`: Deleta um livro.
- `GET /api/books`: Lista todos os livros.
- `GET /api/books/{id}`: Obtém detalhes de um livro específico (ao pesquisar um livro pelo ID, o contador é incrementado).
- `GET /api/books/google-books`: Pesquisa na API de livros do Google.

Certifique-se de ter os microserviços apropriados em execução para que o gateway possa rotear as solicitações corretamente.

Fique à vontade para contribuir com este projeto.



