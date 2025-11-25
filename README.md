# Produtos-Naturais-Granel-


1️⃣ Objetivo do Projeto 🏗️

O objetivo do projeto foi desenvolver uma API RESTful completa, capaz de:

Cadastrar produtos

Listar produtos

Atualizar produtos

Excluir produtos

Tudo isso usando Node.js + Express e salvando os dados no Supabase.

Essa API servirá como o backend para uma loja de Produtos Naturais a Granel.



2️⃣ Stack do Projeto 🦾

O sistema foi desenvolvido utilizando:

Node.js → ambiente que roda JavaScript no servidor

Express.js → framework para criar rotas e servidor

Supabase (PostgreSQL) → banco de dados online

Nodemon → reinicia o servidor automaticamente

Postman/Insomnia → usado para testar as rotas

Essa combinação permitiu criar uma API profissional e escalável.



3️⃣ Criação do Projeto 📽️

A primeira etapa foi criar o projeto no terminal:

npm init -y


Isso gerou o package.json, onde ficam:

Dependências

Scripts

Informações do projeto.



4️⃣ Pacotes Instalados 📦

Com o projeto criado, instalamos as dependências necessárias:

npm install express cors


E também:

npm install --save-dev nodemon


express: criação das rotas

cors: permitir acesso de aplicações externas

nodemon: facilita o desenvolvimento.



5️⃣ Configurando o Servidor Express ⌨️

Criamos o arquivo:

server.js


E configuramos o servidor:

const express = require('express');
const app = express();
app.use(express.json());
app.listen(3000);


Aqui definimos:

Porta de acesso

Interpretação de JSON

Inicialização do servidor.



6️⃣ Integração com Supabase 🧠

No Supabase:

Criamos um projeto

Criamos uma tabela produtos com os campos:

id

nome

preço

quantidade

imagem

Depois conectamos ao banco criando o arquivo:

src/database/supabase.js


com a chave e URL gerada pelo Supabase.

A partir daí, todas as operações CRUD passaram a salvar dados diretamente no banco.



7️⃣ Rotas da API 🗺️

A API possui rotas REST, como:

GET     /produtos
GET     /produtos/:id
POST    /produtos
PUT     /produtos/:id
DELETE  /produtos/:id


Cada rota responde a uma operação específica.



8️⃣ CRUD 💾

CRUD significa:

Create → POST
Cadastra novos produtos

Read → GET
Lista produtos

Update → PUT
Atualiza dados

Delete → DELETE
Remove um produto

Esse conjunto de funções transforma a API em um sistema completo de gerenciamento.



9️⃣ Testes com Postman 🧑‍💻

Cada rota foi testada usando ferramentas como:

Postman

Insomnia

Thunder Client

Nesses testes verificamos:

Se o banco recebia os dados

Se as rotas retornavam as mensagens corretas

Se havia tratamento de erros.



🔟 Estrutura Final do Projeto 🏛️

A organização final do código ficou assim:

/src
   /routes
      produtosRoutes.js
   /controllers
      produtosController.js
   /database
      supabase.js

server.js


Essa estrutura separa:

Rotas

Lógica de negócios

Conexão com o banco

Deixando o código mais legível e profissional.



1️⃣1️⃣ Conclusão 🗃️

O projeto entregue resultou em uma API:

Profissional

Organizada

Conectada a um banco real

Com todos os recursos CRUD

Pronta para ser integrada com:

Sites

Aplicativos

Painéis administrativos

E pode ser evoluída com:

Login e autenticação

Categorias

Clientes e pedidos

Relatórios e dashboards
