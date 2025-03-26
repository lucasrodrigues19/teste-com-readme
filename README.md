# API de Produtos

Este é um projeto para a criação de uma aplicação CRUD de produtos, onde serão avaliados conhecimentos em React, JavaScript, Java e Spring Framework. A aplicação terá uma API REST para manipulação de pedidos, produtos e categorias, e um frontend para gerenciamento e visualização das informações.

## Objetivo

A aplicação permite o gerenciamento de  **pedidos**, **produtos** e suas **categorias**, possibilitando que o usuário:

- Crie e exclua pedidos
- Crie, leia, atualize e exclua produtos.
- Crie, leia, atualize e exclua categorias.

## Estrutura do Projeto

### Backend (Spring Boot + Java)

- **Spring Boot** será utilizado para a criação da API REST.
- **Banco de Dados**: O projeto utilizará o **H2** para armazenar as informações de pedido, produtos e categorias.
- **Requisitos**:
  - CRUD para pedidos, produtos e categorias.
  - Relacionamento entre **Produto** e **Categoria** (N-1).
  - Relacionamento entre **Pedido** e **Produto** (N-1).

### Frontend (React + JavaScript + Next)

- **React + Next** será utilizado para a criação do frontend da aplicação.
- A interface permitirá visualizar a tabela de peditos, produtos e categorias, com filtros e opções de edição.
- A aplicação fará chamadas à API REST para realizar as operações de CRUD.
- **Funcionalidades**:
    - **Produtos**
      - Tabela com a listagem dos produtos.
      - Filtros para buscar produtos por nome, preço e categoria.
      - Formulários para adicionar, editar e excluir produtos.

  - **Categorias**
      - Tabela com a listagem das categorias.
      - Filtro para buscar categorias por nome.
      - Formulários para adicionar, editar e excluir categorias.

  - **Pedidos**
      - Tabela com a listagem das pedidos, mostrando os produtos, valor individual de cada produto e o valor total do pedido.
      - Filtros para buscar pedidos por id e data.
      - Formulários para adicionar e excluir pedidos.

## Critérios Avaliados

1. **Legibilidade**:
   - O código deve ser bem estruturado e fácil de entender.
   - Nomes de variáveis e funções devem ser claros e descritivos.

2. **Controle de versão**:
   - O uso de **git** para versionamento do código será fundamental.
   - É importante que as alterações sejam feitas de forma organizada, com commits claros e frequentes.

3. **Simplicidade do código**:
   - O código deve ser simples, objetivo e sem complexidade desnecessária.
   - A aplicação deve ser fácil de entender, com a menor quantidade de código possível para atingir o objetivo.

4. **Manipulação com o banco de dados**:
   - As operações de CRUD devem ser feitas corretamente, utilizando **JPA** ou **Spring Data** para interação com o banco de dados.

5. **Manipulação da API REST**:
   - A API deve ser bem estruturada e as rotas (endpoints) devem seguir boas práticas RESTful.
   - A comunicação entre o frontend e o backend deve ser eficiente, com o uso adequado de métodos HTTP (GET, POST, PUT, DELETE).

6. **Conceitos de Frontend**:
   - A aplicação deve ser responsiva, utilizando boas práticas de **React**.
   - O uso de componentes deve ser modular, reutilizável e de fácil manutenção.
   - A interface deve ser clara e simples, com foco na usabilidade.

7. **Tempo para resolver o problema**:
   - A solução deve ser entregue dentro de um prazo razoável. O foco está na qualidade do código, mas também no tempo de desenvolvimento.

8. **Programação Orientada a Objetos (POO)**:
   - As entidades e lógicas de negócio devem ser bem definidas e organizadas usando conceitos de POO.
   - O código deve ser modular, reutilizável e fácil de manter.


## Passo a Passo para Configuração

### 1. Configuração do Ambiente

#### Backend (Spring Boot + Java)

1. *Em seu workspace, abra o git bash e  clone esse repositorio, com o comando*:
```bash
git clone https://github.com/bv-roberti/Interview-template.git

```
2. *No diretorio do seu projeto, abra o git bash e ultilize a url do seu projeto para o seu repositorio, com o comando*:
```bash
git remote set-url https://github.com/bv-roberti/<seu_repositorio>.git

```
3. *Importe o projeto no Eclipse*:
   bash
   File > Import > Existing Maven Projects > Selecione a pasta backend, que se encontra no diretório do projeto
   
 *Para exexutar o projeto no Eclipse*:
   bash
   Debug As > Spring Boot App/Java application
   
**A aplicação vai rodar  em http://localhost:8080**

**Para acessar o banco: http://localhost:8080/h2-console**

#### Frontend (React + JavaScript + Next)

**Usar o yarn para gerenciar as dependencias.**

6. No visual studio, abra um workspace na pasta frontend, que se encontra no diretorio do seu projeto.

Para inciar o serviço de desenvolvimento, abra o terminal na pasta frontend e rode um dos comandos abaixo:

```bash
yarn dev (Linux e MAC OS)
# or
yarn start-dev-windows (Windows)

```
**A aplicação vai rodar  em http://localhost:3005**
   

### 2. Desenvolvimento do Backend
#### Estrutura MVC
**portal.web.permits.produtos.entities**  Entidades

**portal.web.permits.produtos.restcontrollers** Controladores/endpoints

**portal.web.permits.produtos.services** Camada de serviço

**portal.web.permits.produtos.repositorys** Repositorio para comunicação com o banco de dados

1. *Crie as entidades*:
   - Produto (id, nome, preço, categoria).
   - Categoria (id, nome).
   - Pedido (id, data, lista de produtos).
2. *Configure os repositórios* utilizando JpaRepository.
3. *Crie os controladores REST* com os endpoints:
   - GET /produtos
   - POST /produtos
   - PUT /produtos/{id}
   - DELETE /produtos/{id}

   - GET /categorias
   - POST /categorias
   - PUT /categorias/{id}
   - DELETE /categorias/{id}

   - GET /pedidos
   - POST /pedidos
   - PUT /pedidos/{id}
   - DELETE /pedidos/{id}
5. *Testar os endpoints* usando Postman ou Insomnia.

**A estrutura do banco será criada de acordo com as definições usadas nas entidades.**

**Fique atento que, sempre que a aplicação for iniciada a estrutura será criada novamente.**

**Os dados no banco só vão estar disponiveis enquanto a aplicação estiver UP**
### 3. Desenvolvimento do Frontend

#### Estrutura
**public:** Serve para adicionar arquivos e recursos para css, imagens ou javascript

**src/api:** Diretorio para arquivos que farão requests ao servidor

**src/app:** Rotas com componentes para logica de negocio

**src/app/i18n:** Configuração da internacionalização

**src/components:** Diretorio com componentes que podem ser reutilizados

**src/configs:** Diretorios para configurações de variaveis ou componentes

**src/context:** Diretorio para componentes do tipo Context

**src/hooks:** Diretorio para Hooks customizados

**src/ui:** Diretorio para componentes com a logica de apresentação das rotas(onde ficam os componentes dos page.js).

**src/utils:** funções utilitarias

**Em cada componente, se usar algum hook, ou função com manipulação de DOM, será necessário adicionar "use client" no inicio do arquivo.**

1. *Crie componentes principais*:
   - src/app/produtos/page.js: exibe a lista de produtos.
   - src/app/produtos/form/page.js: formulário para adicionar/editar produtos.

   - src/app/categorias/page.js: exibe a lista de categorias.
   - src/app/categorias/form/page.js: formulário para adicionar/editar categorias.

   - src/app/pedidos/page.js: exibe a lista de pedidos.
   - src/app/pedidos/form/page.js: formulário para adicionar/editar pedidos.

2. *Consuma a API do backend* usando Axios.
3. *Implemente filtros* para buscar produtos por nome, preço e categoria.
4. *Teste as funcionalidades no navegador*.

### 4. Controle de Versão

1. *Crie um repositório no GitHub*.
2. *Adicione o projeto ao Git*:
   bash
   git init
   git add .
   git commit -m "Projeto inicial"
   git branch -M main
   git remote add origin <URL_DO_REPOSITORIO>
   git push -u origin main
   
3. *Mantenha commits frequentes e organizados*.

### 5. Testes e Entrega

1. *Teste todas as funcionalidades* para garantir que tudo funciona corretamente.
2. *Escreva um README* com instruções para rodar o projeto.
3. *Submeta o projeto no GitHub* e compartilhe o link.
