📖 Livraria API — Visão Geral do Projeto
Uma API REST desenvolvida em Python para gerenciamento de um acervo de livros, construída sobre o FastAPI e apoiada por um banco MySQL. O sistema oferece todas as operações clássicas de persistência — criação, leitura, edição e remoção — e ainda entrega uma interface web que consome esses recursos, permitindo que qualquer pessoa gerencie o catálogo sem tocar em código.

🧩 Peças que Compõem o Projeto
O funcionamento da aplicação depende de um conjunto de bibliotecas, cada uma com uma responsabilidade bem definida:

FastAPI — desenha as rotas da aplicação e ainda gera, de forma automática, uma documentação interativa pronta para uso.

Uvicorn — é o servidor que coloca tudo no ar, rodando a aplicação ASGI.

SQLAlchemy — faz a ponte entre o código Python e as tabelas do banco, traduzindo objetos em registros.

PyMySQL — driver que permite ao SQLAlchemy dialogar com o MySQL.

Pydantic Settings — centraliza e organiza as configurações e variáveis de ambiente.

Python Dotenv — lê os valores guardados no arquivo .env, mantendo dados sensíveis fora do código.

MySQL — banco de dados onde os livros ficam armazenados.

Frontend — camada visual que consome a API e executa o CRUD pelo navegador.

🗄️ Estrutura de Persistência
A comunicação com o MySQL está estabelecida e validada. Toda a camada de dados foi montada com SQLAlchemy aliado ao PyMySQL, cobrindo desde a configuração até a definição do modelo.

Foram executadas as seguintes etapas:

Leitura das credenciais do banco a partir de variáveis de ambiente;

Montagem do engine de conexão;

Criação da sessão responsável pelas operações;

Definição do modelo que representa um Livro dentro do banco;

Padronização desse modelo;

Estruturação pronta para receber todas as operações de CRUD.

🌐 Rotas Disponíveis
A API expõe cinco endpoints principais:

POST — insere um novo livro no acervo;

GET — devolve a lista completa de livros cadastrados;

GET /{id} — recupera um livro específico a partir do seu identificador;

PUT — altera os dados de um livro já existente;

DELETE — apaga um livro pelo seu ID.

🔁 Cobertura do CRUD
Create — cadastro de novos livros;

Read — listagem geral e consulta individual;

Update — edição de registros existentes;

Delete — remoção de livros.

🖥️ Interface Web
Além da API, o projeto conta com um frontend que consome os endpoints e permite gerenciar os livros de forma visual.

O que já foi entregue nessa camada:

Estrutura inicial do frontend;

Página dedicada aos livros;

Layout da interface;

Conexão com a API;

Integração das operações de CRUD;

Validação do cadastro pela interface;

Validação da listagem e consulta;

Validação da atualização;

Validação da exclusão;

Execução e testes locais.

A interface segue o contrato definido pela API para disparar as requisições, permitindo testar todas as operações de forma gráfica.

🧪 Verificações Realizadas
Ao longo do desenvolvimento, foram conduzidos testes para confirmar o funcionamento de cada parte:

Inicialização da API;

Conexão com o banco;

Rota POST de cadastro;

Rota GET de listagem;

Consulta por ID;

Rota PUT de atualização;

Rota DELETE de exclusão;

Confirmação das rotas completas do CRUD;

Validação do CRUD completo pelo Swagger;

Integração entre frontend e API;

Execução local do frontend;

Validação do CRUD completo pela interface.

📚 Documentação Automática
O FastAPI gera a documentação da API sem esforço adicional, disponível em dois formatos:

Swagger UI → /docs

ReDoc → /redoc

Por meio delas é possível consultar todas as rotas, visualizar o contrato da API e testar as operações diretamente no navegador. Esse contrato foi validado e serviu de base para a integração com o frontend.

🚧 Caminho Percorrido no Desenvolvimento
O projeto foi construído em blocos, começando pela organização do repositório e do ambiente, passando pela configuração da API e do banco, criação das rotas de cadastro e consulta, implementação do CRUD completo e, por fim, o desenvolvimento e a integração do frontend.

Organização do repositório;

Instalação das dependências;

Estrutura inicial da aplicação;

Proteção das configurações locais;

Configuração da conexão com o MySQL;

Criação da aplicação FastAPI e rota de saúde;

Validação da inicialização da API;

Validação da conexão com o banco;

Preparação do ambiente para a etapa 2;

Criação do modelo de livros;

Criação dos schemas de livros;

Criação da sessão do banco;

Rota de cadastro de livros;

Rota de listagem de livros;

Consulta de livro por ID;

Atualização das dependências;

Correções no banco de dados;

Validação das rotas POST e GET;

Atualização da documentação do banco;

Preparação do ambiente para a etapa 3;

Padronização do modelo de livros;

Padronização dos schemas de livros;

Preparação do arquivo principal para o CRUD;

Rota de atualização de livros;

Rota de exclusão de livros;

Confirmação das rotas completas do CRUD;

Validação do CRUD completo pelo Swagger;

Confirmação do contrato da API para o frontend;

Preparação da estrutura do frontend;

Criação da página de livros;

Desenvolvimento do layout;

Conexão do frontend ao CRUD;

Documentação do funcionamento do frontend;

Execução local do frontend;

Validação do CRUD completo pelo frontend.

📝 Registro de Commits
Início do Projeto
text
chore: inicia repositorio da api de livros
chore: prepara pasta do projeto
chore: adiciona dependencias da api
chore: cria estrutura inicial da aplicacao
chore: protege configuracoes locais
Configuração da API e Banco de Dados
text
feat: configura conexao com mysql
feat: cria aplicacao fastapi e rota de saude
test: valida inicializacao da api
test: valida conexao com banco de dados
feat readme
Desenvolvimento das Funcionalidades
text
chore: prepara ambiente para a parte 2
feat: cria modelo de livros
feat: adiciona schemas de livros
feat: cria sessao do banco
feat: cria rota para cadastrar livros
feat: cria rota para listar livros
feat: cria consulta de livro por id
atualizando req.txt
Fix(Banco de dados)
test: valida rotas post e get
docs: atualiza banco apos rotas de cadastro e consulta
Desenvolvimento do CRUD
text
chore: prepara ambiente para a parte 3
fix: padroniza modelo livro
fix: padroniza schemas de livros
fix: prepara arquivo principal para crud
feat: cria rota para atualizar livros
feat: cria rota para excluir livros
test: confirma rotas completas do crud
test: valida crud completo pelo swagger
docs: confirma contrato da api para frontend
Desenvolvimento do Frontend
text
docs: prepara integracao do frontend
feat: permite acesso do frontend
chore: cria estrutura do frontend
feat: cria pagina de livros
style: adiciona layout do frontend
feat: conecta frontend ao crud de livros
docs: explica funcionamento do frontend
test: executa frontend localmente
test: valida crud pelo frontend
📈 Situação Atual
A API está de pé, com o FastAPI configurado e o MySQL devidamente conectado. O banco opera normalmente, o modelo de livros e os schemas foram criados e padronizados, e a sessão do banco está pronta para uso.

Todas as funcionalidades do CRUD — cadastro, listagem, consulta por ID, atualização e exclusão — estão operacionais. As rotas POST, GET, PUT e DELETE passaram por testes e foram validadas pelo Swagger, com o contrato da API confirmado para o frontend.

No frontend, a estrutura foi montada, a página de livros está no ar, o layout foi implementado e a conexão com a API está ativa. O CRUD foi integrado à interface, que já rodou localmente com todas as operações validadas.

A documentação encontra-se atualizada. O projeto permanece em desenvolvimento.