📚 API de Biblioteca
<div align="center">
🏫 Projeto de Programação — 3º Ano do Ensino Médio

Uma API REST para gerenciamento de livros, usuários e empréstimos de uma biblioteca.

<br>







<br>






</div>
📖 Sobre o Projeto

A API de Biblioteca é um projeto desenvolvido para a disciplina de Programação do 3º ano do Ensino Médio, durante o 3º bimestre.

O objetivo é desenvolver uma API REST capaz de simular o funcionamento básico de uma biblioteca, permitindo o gerenciamento de:

📚 Livros
👤 Usuários
🔄 Empréstimos
↩️ Devoluções

O projeto também tem como finalidade colocar em prática conceitos de Python, APIs REST, bancos de dados, organização de código, Git e desenvolvimento de software.

💡 Objetivo principal: transformar os conhecimentos adquiridos em sala de aula em uma aplicação funcional.

🎯 Objetivos

O projeto busca desenvolver uma API simples, organizada e funcional para gerenciamento de uma biblioteca.

Principais funcionalidades
Funcionalidade	Descrição
📖 Livros	Cadastrar, consultar, atualizar e remover livros
👤 Usuários	Cadastrar e consultar usuários
🔎 Consultas	Buscar registros específicos
✏️ Atualizações	Alterar informações cadastradas
🗑️ Remoções	Excluir registros
📚 Empréstimos	Registrar empréstimos de livros
↩️ Devoluções	Registrar a devolução de livros
🗄️ Banco de dados	Armazenar as informações da biblioteca
🛠️ Tecnologias Utilizadas
<div align="center">
Tecnologia	Utilização
🐍 Python	Linguagem principal
⚡ FastAPI	Desenvolvimento da API
🗃️ SQLite	Banco de dados
🔗 REST API	Arquitetura da aplicação
📦 JSON	Formato de troca de dados
🌿 Git	Controle de versão
🐙 GitHub	Hospedagem e colaboração
</div>
🏗️ Arquitetura do Projeto

A aplicação segue uma organização modular, separando responsabilidades entre diferentes partes do projeto.

📦 api-biblioteca
│
├── 📂 app
│   │
│   ├── 📄 main.py
│   │
│   ├── 📂 models
│   │   └── 🗃️ Modelos do banco de dados
│   │
│   ├── 📂 routes
│   │   └── 🔗 Rotas/endpoints da API
│   │
│   ├── 📂 database
│   │   └── 🗄️ Configuração do banco de dados
│   │
│   └── 📂 schemas
│       └── 📋 Schemas e validações
│
├── 📂 tests
│   └── 🧪 Testes automatizados
│
├── 📄 requirements.txt
├── 📄 README.md
└── 📄 .gitignore

🚀 Como Executar o Projeto
📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

🐍 Python
🌿 Git
💻 Um terminal
✏️ Um editor de código, como VS Code
1️⃣ Clonar o repositório
git clone URL_DO_REPOSITORIO


Depois, entre na pasta:

cd api-biblioteca

2️⃣ Criar o ambiente virtual
Windows
python -m venv venv

Linux / macOS
python3 -m venv venv

3️⃣ Ativar o ambiente virtual
🪟 Windows — CMD
venv\Scripts\activate

🪟 Windows — PowerShell
venv\Scripts\Activate.ps1

🐧 Linux / 🍎 macOS
source venv/bin/activate


Após a ativação, o terminal deverá apresentar algo semelhante a:

(venv) C:\...\api-biblioteca>

4️⃣ Instalar as dependências

Com o ambiente virtual ativado:

pip install -r requirements.txt

5️⃣ Executar a API

Utilize:

uvicorn app.main:app --reload


Se tudo estiver configurado corretamente, será exibida uma mensagem semelhante a:

INFO:     Uvicorn running on http://127.0.0.1:8000


🎉 A API estará funcionando localmente!

🌐 Acessando a API

Depois de iniciar o servidor, acesse:

🔗 API
http://127.0.0.1:8000

📘 Swagger UI
http://127.0.0.1:8000/docs

📗 ReDoc
http://127.0.0.1:8000/redoc


⭐ O Swagger UI permite visualizar e testar os endpoints diretamente pelo navegador.

🔗 Endpoints
📚 Livros
Método	Endpoint	Descrição
🟢 GET	/livros	Lista todos os livros
🟢 GET	/livros/{id}	Busca um livro específico
🔵 POST	/livros	Cadastra um novo livro
🟡 PUT	/livros/{id}	Atualiza um livro
🔴 DELETE	/livros/{id}	Remove um livro
👤 Usuários
Método	Endpoint	Descrição
🟢 GET	/usuarios	Lista todos os usuários
🟢 GET	/usuarios/{id}	Busca um usuário específico
🔵 POST	/usuarios	Cadastra um novo usuário
🟡 PUT	/usuarios/{id}	Atualiza um usuário
🔴 DELETE	/usuarios/{id}	Remove um usuário
🔄 Empréstimos
Método	Endpoint	Descrição
🔵 POST	/emprestimos	Registra um empréstimo
🟢 GET	/emprestimos	Lista os empréstimos
🟡 PUT	/emprestimos/{id}/devolver	Registra uma devolução
📦 Exemplo de Requisição
➕ Cadastrar um livro
POST /livros
{
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano": 1899
}

📥 Resposta esperada
{
    "id": 1,
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano": 1899
}

🔄 Fluxo da Biblioteca

O funcionamento básico da aplicação pode ser representado assim:

                📚 API DE BIBLIOTECA
                        │
                        ▼
              ┌───────────────────┐
              │    👤 Usuários    │
              └─────────┬─────────┘
                        │
                        ▼
              ┌───────────────────┐
              │    📖 Livros      │
              └─────────┬─────────┘
                        │
                        ▼
              ┌───────────────────┐
              │  🔄 Empréstimo    │
              └─────────┬─────────┘
                        │
                        ▼
              ┌───────────────────┐
              │  ↩️ Devolução     │
              └─────────┬─────────┘
                        │
                        ▼
              ┌───────────────────┐
              │ 🗄️ Banco SQLite   │
              └───────────────────┘

📅 Etapas do Projeto

O projeto será desenvolvido em 4 etapas, com uma etapa sendo realizada a cada quarta-feira na escola.

🟦 Etapa 1 — Planejamento e Estrutura

Objetivo: definir o funcionamento da API e criar a estrutura inicial do projeto.

Atividades
 🎯 Definir o objetivo da API
 📝 Planejar as funcionalidades
 📁 Criar a estrutura de pastas
 🐍 Configurar o ambiente Python
 📦 Instalar as dependências
 🔗 Criar o primeiro endpoint de teste
🟩 Etapa 2 — Livros e Usuários

Objetivo: implementar os principais cadastros da biblioteca.

Atividades
 📖 Criar cadastro de livros
 👤 Criar cadastro de usuários
 📋 Criar endpoints para listar registros
 🔎 Criar endpoints para buscar registros específicos
 🧪 Realizar testes das funcionalidades
🟨 Etapa 3 — Empréstimos e Banco de Dados

Objetivo: implementar o sistema de empréstimos e integrar a aplicação ao banco de dados.

Atividades
 🗄️ Configurar o SQLite
 📊 Criar as tabelas necessárias
 📚 Implementar empréstimos
 ↩️ Implementar devoluções
 🔗 Relacionar livros e usuários
 🧪 Testar as operações da API
🟥 Etapa 4 — Finalização e Testes

Objetivo: realizar os ajustes finais e preparar o projeto para apresentação.

Atividades
 🐛 Corrigir possíveis erros
 🧪 Testar todos os endpoints
 🧹 Organizar o código
 📚 Melhorar a documentação
 📝 Finalizar o README
 🎤 Apresentar o projeto
📊 Progresso
┌──────────────────────────────────────────────┐
│              🚧 PROJETO EM ANDAMENTO         │
├──────────────────────────────────────────────┤
│                                              │
│  🟦 Etapa 1  ████████████████████  100%     │
│  🟩 Etapa 2  ░░░░░░░░░░░░░░░░░░░░    0%     │
│  🟨 Etapa 3  ░░░░░░░░░░░░░░░░░░░░    0%     │
│  🟥 Etapa 4  ░░░░░░░░░░░░░░░░░░░░    0%     │
│                                              │
└──────────────────────────────────────────────┘


🚧 Status atual: Em desenvolvimento.

🧪 Testes

Os testes serão utilizados para verificar se os principais recursos da API estão funcionando corretamente.

A estrutura planejada é:

📂 tests
│
├── 🧪 test_livros.py
├── 🧪 test_usuarios.py
└── 🧪 test_emprestimos.py


Para executar os testes, futuramente:

pytest

🗄️ Banco de Dados

O projeto utiliza SQLite para armazenamento das informações.

O banco será responsável por armazenar dados relacionados a:

📖 Livros
   │
   ├── ID
   ├── Título
   ├── Autor
   └── Ano
       
👤 Usuários
   │
   ├── ID
   ├── Nome
   └── Informações do usuário

🔄 Empréstimos
   │
   ├── ID
   ├── Livro
   ├── Usuário
   ├── Data do empréstimo
   └── Data da devolução

🔐 Boas Práticas

Durante o desenvolvimento serão utilizados conceitos de organização e boas práticas, como:

📂 Separação de responsabilidades
🧹 Código organizado
📝 Documentação
🌿 Controle de versões com Git
🧪 Testes
🔒 Validação de dados
📦 Ambiente virtual
🔗 Arquitetura REST
🗺️ Roadmap
                    API DE BIBLIOTECA
                           │
                           ▼
              ┌──────────────────────┐
              │ 📝 Planejamento      │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ 📖 Livros            │
              │ 👤 Usuários          │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ 🗄️ Banco de Dados   │
              │ 🔄 Empréstimos      │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ 🧪 Testes            │
              │ 🐛 Correções         │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ 🚀 Projeto Finalizado│
              └──────────────────────┘

🎓 Projeto Escolar

Este projeto foi desenvolvido como atividade prática da disciplina de Programação do 3º ano do Ensino Médio, durante o 3º bimestre.

O principal objetivo é aplicar, na prática, conhecimentos relacionados a:

🐍 Python
     +
⚡ FastAPI
     +
🗄️ Banco de Dados
     +
🔗 APIs REST
     +
🌿 Git
     +
🐙 GitHub
     ↓
🚀 Desenvolvimento de Software


Mais do que criar uma API, o projeto busca proporcionar experiência com o processo de desenvolvimento de uma aplicação real.

👨‍💻 Desenvolvedores

Projeto desenvolvido pelos alunos do 3º ano do Ensino Médio.

<div align="center">
📚 API de Biblioteca

Programação • 3º Bimestre • Projeto Escolar

<br>

⭐ Se este projeto foi útil ou interessante, considere deixar uma estrela no repositório!

<br>

Feito com 🐍 Python + ⚡ FastAPI + 🗄️ SQLite

</div>
<div align="center">
🚧 Projeto em desenvolvimento 🚧

v1.0.0 • 2026

</div>