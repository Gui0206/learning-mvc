# Explique com suas palavras o funcionamento do models, controller e fale sobre endpoints no projeto.

#### Explique com suas palavras o papel de cada camada da arquitetura MVC usada neste projeto. Como o Model, o Controller e a View interagem entre si?

Primeiro explicarei as views: Elas são o que guardam o código HTML, que é a interface visível para o usuário.  
Quando apertamos um botão na página, ele é recebido por uma rota, e o controller cria a requisição para o model.  
Já no model uma query SQL é usada para interagir com o banco de dados.

#### Como ocorre o envio e o recebimento de dados no formato JSON neste projeto? Cite uma rota que responde em JSON e explique seu funcionamento.

`router.post('/edit/:id', controller.update);`  
Essa rota envia um JSON com as informações da requisição, e o ID desejado.

#### Qual a importância de usar HTML básico com formulários e tabelas para organizar e manipular dados no navegador? Por que esse tipo de estrutura ainda é útil em projetos back-end com Node.js?

Pois é com ele que criamos a estrutura de interface interagível para o usuário.



# Explique com suas palavras o funcionamento do models, controller e fale  sobre endpoints no projeto.
Em models temos as consultas SQL para cada tabela do database, por exemplo; No arquivo aluno.js podemos interagir com a tabela alunos.
Os controllers recebem a requisição vinda do usuário, (req) e mandam a resposta para os models (res).

-------------------

# Boilerplate MVC em Node.js com PostgreSQL

Este projeto é um boilerplate básico para uma aplicação Node.js seguindo o padrão MVC (Model-View-Controller), utilizando PostgreSQL como banco de dados.

## Requisitos

- Node.js (versão X.X.X)
- PostgreSQL (versão X.X.X)

## Instalação

1. **Clonar o repositório:**

```bash
   git clone https://github.com/seu-usuario/seu-projeto.git
   cd seu-projeto
```

2. **Instalar as dependências:**
    
```bash
npm install
```
    
3. **Configurar o arquivo `.env`:**
    
Renomeie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente necessárias, como as configurações do banco de dados PostgreSQL.
    

Configuração do Banco de Dados
------------------------------

1. **Criar banco de dados:**
    
    Crie um banco de dados PostgreSQL com o nome especificado no seu arquivo `.env`.
    
2. **Executar o script SQL de inicialização:**
    
```bash
npm run init-db
```
    
Isso criará a tabela `users` no seu banco de dados PostgreSQL com UUID como chave primária e inserirá alguns registros de exemplo.
    

Funcionalidades
---------------

* **Padrão MVC:** Estrutura organizada em Model, View e Controller.
* **PostgreSQL:** Banco de dados relacional utilizado para persistência dos dados.
* **UUID:** Utilização de UUID como chave primária na tabela `users`.
* **Scripts com `nodemon`:** Utilização do `nodemon` para reiniciar automaticamente o servidor após alterações no código.
* **Testes:** Inclui estrutura básica para testes automatizados.

Scripts Disponíveis
-------------------

* `npm start`: Inicia o servidor Node.js.
* `npm run dev`: Inicia o servidor com `nodemon`, reiniciando automaticamente após alterações no código.
* `npm run test`: Executa os testes automatizados.
* `npm run test:coverage`: Executa os testes e gera um relatório de cobertura de código.

Estrutura de Diretórios
-----------------------

* **`config/`**: Configurações do banco de dados e outras configurações do projeto.
* **`controllers/`**: Controladores da aplicação (lógica de negócio).
* **`models/`**: Modelos da aplicação (definições de dados e interações com o banco de dados).
* **`routes/`**: Rotas da aplicação.
* **`tests/`**: Testes automatizados.
* **`views/`**: Views da aplicação (se aplicável).

Contribuição
------------

Contribuições são bem-vindas! Sinta-se à vontade para abrir um issue ou enviar um pull request.

Licença
-------

Este projeto está licenciado sob a Licença MIT.

Este README.md fornece uma visão geral clara do boilerplate, incluindo instruções de instalação, configuração do banco de dados, funcionalidades principais, scripts disponíveis, estrutura de diretórios, como contribuir e informações de licença. Certifique-se de personalizar as seções com detalhes específicos do seu projeto conforme necessário.