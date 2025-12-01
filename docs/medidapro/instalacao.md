# Instalação e Execução

Este guia descreve como configurar o ambiente e executar o MedidaPro.

## Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:

*   **Java JDK 21**: Necessário para compilar e rodar a aplicação.
*   **Maven**: Para gerenciamento de dependências e build (embora o projeto inclua o wrapper `mvnw`).
*   **Docker**: Para executar containers, se desejado.
*   **Banco de Dados SQL Server**: A aplicação espera uma conexão com um banco SQL Server.

## Executando com Spring Boot

A maneira mais simples de rodar a aplicação para desenvolvimento é utilizando o plugin do Spring Boot via Maven.

### Via Linha de Comando

No diretório `app/`, execute:

```bash
# Linux/macOS
./mvnw spring-boot:run

# Windows
mvnw spring-boot:run
```

A aplicação estará disponível em `http://localhost:8080/`.

### Via IDE (IntelliJ / Eclipse)

1.  Importe o projeto como um projeto Maven.
2.  Localize a classe `Application.java` (em `src/main/java/br/dev/sym/medidapro/Application.java`).
3.  Execute a classe como uma aplicação Java.

## Executando em Modo de Produção

Para rodar em modo de produção (otimizado para o Vaadin), utilize o perfil `production`:

```bash
./mvnw spring-boot:run -Pproduction
```

## Configuração do Banco de Dados

Certifique-se de que as configurações de conexão com o banco de dados no arquivo `application.properties` (ou `application.yml`) estejam corretas para o seu ambiente.

Exemplo de configuração típica:

```properties
spring.datasource.url=jdbc:sqlserver://localhost:1433;databaseName=MedidaPro;encrypt=true;trustServerCertificate=true;
spring.datasource.username=sa
spring.datasource.password=sua_senha_forte
spring.jpa.hibernate.ddl-auto=update
```

## Docker

O projeto inclui um `Dockerfile`. Para construir e rodar a imagem:

1.  **Build da Imagem:**
    ```bash
    docker build -t medidapro:latest .
    ```

2.  **Executar Container:**
    ```bash
    docker run -p 8080:8080 medidapro:latest
    ```