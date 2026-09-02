📚 API de Biblioteca

Projeto desenvolvido para a disciplina de programação do 3º ano do Ensino Médio, durante o 3º bimestre.

O objetivo do projeto é desenvolver uma API de gerenciamento de biblioteca utilizando Python, permitindo cadastrar, consultar, atualizar e remover informações relacionadas a livros e usuários.

🎯 Objetivo do Projeto

Criar uma API simples para simular o funcionamento de uma biblioteca, utilizando conceitos de programação, banco de dados e desenvolvimento de APIs.

Durante o projeto serão desenvolvidas funcionalidades como:

📖 Cadastro de livros
👤 Cadastro de usuários
🔎 Consulta de livros e usuários
✏️ Atualização de informações
🗑️ Remoção de registros
📚 Controle de empréstimos e devoluções
🛠️ Tecnologias
Python
FastAPI
SQLite
Git e GitHub
REST API
JSON
📅 Etapas do Projeto

O projeto será desenvolvido em 4 etapas, sendo uma etapa realizada a cada quarta-feira na escola.

1ª Etapa — Planejamento e Estrutura

Nesta primeira etapa será definido o funcionamento da API e criada a estrutura inicial do projeto.

Atividades:

Definir o objetivo da API
Planejar as funcionalidades
Criar a estrutura de pastas
Configurar o ambiente Python
Instalar as dependências
Criar o primeiro endpoint de teste
2ª Etapa — Livros e Usuários

Nesta etapa serão criados os principais cadastros da biblioteca.

Atividades:

Criar o cadastro de livros
Criar o cadastro de usuários
Criar endpoints para listar os registros
Criar endpoints para buscar registros específicos
Realizar testes das funcionalidades
3ª Etapa — Empréstimos e Banco de Dados

Nesta etapa será implementado o sistema de empréstimos e a integração com o banco de dados.

Atividades:

Configurar o banco de dados SQLite
Criar as tabelas necessárias
Implementar empréstimos
Implementar devoluções
Relacionar livros e usuários
Testar as operações da API
4ª Etapa — Finalização e Testes

Na última etapa serão realizados os ajustes finais e a documentação do projeto.

Atividades:

Corrigir possíveis erros
Testar todos os endpoints
Organizar o código
Melhorar a documentação
Finalizar o README
Apresentar o projeto
📁 Estrutura do Projeto
api-biblioteca/
│
├── app/
│   ├── main.py
│   ├── models/
│   ├── routes/
│   ├── database/
│   └── schemas/
│
├── tests/
│
├── requirements.txt
├── README.md
└── .gitignore

▶️ Como executar o projeto
1. Clonar o repositório
git clone URL_DO_REPOSITORIO

2. Entrar na pasta
cd api-biblioteca

3. Criar um ambiente virtual
python -m venv venv

4. Ativar o ambiente virtual

No Windows:

venv\Scripts\activate


No Linux/Mac:

source venv/bin/activate

5. Instalar as dependências
pip install -r requirements.txt

6. Executar a API
uvicorn app.main:app --reload


Depois disso, a API estará disponível localmente.

🔗 Endpoints planejados
Método	Endpoint	Descrição
GET	/livros	Lista todos os livros
GET	/livros/{id}	Busca um livro
POST	/livros	Cadastra um livro
PUT	/livros/{id}	Atualiza um livro
DELETE	/livros/{id}	Remove um livro
GET	/usuarios	Lista os usuários
POST	/usuarios	Cadastra um usuário
POST	/emprestimos	Registra um empréstimo
PUT	/emprestimos/{id}/devolver	Registra uma devolução
📌 Status do Projeto

Em desenvolvimento.

 Etapa 1 — Planejamento e estrutura
 Etapa 2 — Livros e usuários
 Etapa 3 — Empréstimos e banco de dados
 Etapa 4 — Finalização e testes
👨‍💻 Projeto Escolar

Projeto desenvolvido como atividade prática do 3º ano do Ensino Médio — 3º bimestre.

O projeto tem como finalidade aplicar conhecimentos de Python, APIs, banco de dados, Git e desenvolvimento de software.