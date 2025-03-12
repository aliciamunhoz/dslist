# Game List API

Este projeto é uma API desenvolvida com Spring Boot e MySQL para gerenciar 
listas de jogos. O sistema permite operações CRUD (Create, Read, Update, 
Delete) tanto para jogos quanto para listas personalizadas, possibilitando 
a organização eficiente de coleções de jogos.

## Tecnologias Utilizadas

- **Java**: Linguagem de programação utilizada para o desenvolvimento da API.
- **Spring Boot**: Framework que facilita a criação de aplicações Java 
robustas e escaláveis.
- **Spring Data JPA**: Abstração para interação com banco de dados relacional.
- **MySQL**: Sistema de gerenciamento de banco de dados relacional 
utilizado para persistência.
- **Maven**: Gerenciador de dependências e automação de build do projeto.

## Funcionalidades

- Cadastro, listagem, busca, atualização e remoção de jogos.
- Criação e gerenciamento de listas de jogos personalizadas.
- Associação de jogos a listas, permitindo melhor organização.

## Configuração do Ambiente

### Pré-requisitos

Antes de iniciar a execução do projeto, é necessário ter instalado:

- **Java 17** ou versão superior.
- **MySQL** para armazenamento dos dados.
- **Maven** para gerenciar as dependências e construir o projeto.

### Configuração do Banco de Dados

1. Crie um banco de dados no MySQL:
   ```sql
   CREATE DATABASE game_list;
   ```
2. Como o intuito deste projeto é para fins educativos, o arquivo 
`application.properties` foi disponibilizado no caminho `src/main/resources`.

## Como Executar o Projeto

Compile e execute o projeto com o Maven:
   ```sh
   mvn spring-boot:run
   ```

## Endpoints Principais

A API disponibiliza os seguintes endpoints para manipulação de jogos e listas:

### Jogos

- **GET** `/games` - Retorna a lista de todos os jogos cadastrados.
- **GET** `/games/{id}` - Busca um jogo específico pelo seu identificador.
- **POST** `/games` - Adiciona um novo jogo ao sistema.
- **PUT** `/games/{id}` - Atualiza as informações de um jogo existente.
- **DELETE** `/games/{id}` - Remove um jogo do banco de dados.

### Listas

- **GET** `/lists` - Retorna todas as listas de jogos criadas.
- **POST** `/lists` - Cria uma nova lista personalizada de jogos.
- **PUT** `/lists/{id}` - Modifica os dados de uma lista existente.
- **DELETE** `/lists/{id}` - Exclui uma lista de jogos.
