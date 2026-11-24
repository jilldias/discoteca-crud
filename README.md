
# Discoteca CRUD

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="MariaDB">
  <img src="https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white" alt="Maven">
</p>

<p align="center">
  <strong>API REST para gerenciamento de álbuns musicais</strong>
</p>

## Sobre o projeto

<div align="justify">

O **Discoteca CRUD** é um projeto de desenvolvimento backend voltado ao gerenciamento de álbuns musicais, construído utilizando Java e Spring Boot.

Inicialmente concebido como uma aplicação Full Stack, o projeto passou por uma reestruturação na qual a camada frontend e arquivos que não eram mais necessários foram removidos. Atualmente, o repositório mantém a estrutura relacionada à API, que está sendo reorganizada e refatorada.

O objetivo desta etapa é aprimorar a arquitetura do backend, melhorar a organização das responsabilidades e consolidar boas práticas de desenvolvimento com Java, Spring Boot, persistência de dados e APIs REST.

</div>

## Estado atual do projeto

<badge color="warning">Em refatoração</badge>

O projeto encontra-se em processo de refatoração. A estrutura atual está concentrada no backend, com foco na reorganização e evolução da API.

As funcionalidades e a arquitetura podem sofrer alterações durante esse processo.

## Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| Java 21 | Linguagem de programação. |
| Spring Boot 4.0.5 | Framework principal da aplicação. |
| Spring Web | Desenvolvimento de APIs REST. |
| Spring Data JPA | Abstração da camada de persistência. |
| Hibernate 7 | Mapeamento objeto-relacional (ORM). |
| MariaDB | Sistema de gerenciamento de banco de dados relacional. |
| Maven | Gerenciamento de dependências e compilação. |

## Arquitetura e organização

<div align="justify">

A aplicação está sendo reorganizada para manter uma separação clara de responsabilidades entre as camadas do backend.

A refatoração busca estabelecer uma estrutura que facilite a manutenção, a evolução das funcionalidades e a integração entre as regras de negócio e a persistência de dados.

</div>

## Requisitos

Para executar o projeto, é necessário possuir:

- JDK 21 ou superior.
- Maven (ou utilizar o Maven Wrapper disponibilizado no projeto).
- MariaDB.
- Git.

## Como executar

### 1. Clonar o repositório

```bash
git clone https://github.com/jilldias/discoteca-crud.git
```

### 2. Acessar o diretório

```bash
cd discoteca-crud
```

### 3. Configurar o banco de dados

Crie um banco de dados no MariaDB e configure as propriedades de conexão no arquivo `src/main/resources/application.properties`.

Exemplo:

```properties
spring.datasource.url=jdbc:mariadb://localhost:3306/discoteca
spring.datasource.username=SEU_USUARIO
spring.datasource.password=SUA_SENHA

spring.datasource.driver-class-name=org.mariadb.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Ajuste as configurações conforme seu ambiente. Não publique credenciais reais no repositório.

### 4. Executar a aplicação

Utilizando o Maven Wrapper:

```bash
./mvnw spring-boot:run
```

Ou utilizando o Maven instalado:

```bash
mvn spring-boot:run
```

Por padrão, o Spring Boot disponibiliza a aplicação em:

```text
http://localhost:8080
```

## Compilação

Para compilar e empacotar a aplicação:

```bash
./mvnw clean package
```

O arquivo JAR será gerado no diretório `target/`.

Para executar o artefato:

```bash
java -jar target/arquivo-gerado.jar
```

## Conceitos e práticas de desenvolvimento

- Desenvolvimento de APIs REST.
- Programação orientada a objetos (POO).
- Separação de responsabilidades.
- Arquitetura em camadas.
- Persistência de dados relacionais.
- Mapeamento objeto-relacional (ORM).
- Integração entre Java, Spring Boot e MariaDB.
- Gerenciamento de dependências com Maven.
- Refatoração e organização de código.

## Refatoração e próximos passos

O desenvolvimento atual está direcionado ao aprimoramento da estrutura backend.

Entre os objetivos de evolução estão:

- Reorganizar pacotes e classes da aplicação.
- Definir responsabilidades claras para cada camada.
- Aprimorar a separação entre entidades, serviços e controladores.
- Revisar os repositórios e operações de persistência.
- Melhorar validações e tratamento de exceções.
- Padronizar as respostas HTTP da API.
- Implementar testes automatizados.
- Aprimorar a documentação dos endpoints.

## Contribuição

Contribuições são bem-vindas!

1. Faça um Fork do projeto.
2. Crie uma branch para sua implementação:

```bash
git checkout -b feature/nova-funcionalidade
```

3. Realize as alterações e registre um commit:

```bash
git commit -m "feat: descreve a alteração"
```

4. Envie sua branch:

```bash
git push origin feature/nova-funcionalidade
```

5. Abra um Pull Request para análise.

## Licença

Projeto desenvolvido para fins educacionais e de aprimoramento em desenvolvimento backend.
