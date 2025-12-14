# Sistema de Gerenciamento de Funcionários (CRUD)

Este é um projeto de estudo desenvolvido em **Django** que implementa um sistema CRUD (Create, Read, Update, Delete) para o gerenciamento de funcionários. O projeto utiliza **MySQL** como banco de dados e **Bootstrap 5** para estilização das interfaces.

## 🚀 Tecnologias Utilizadas

* **Python**
* **Django 6.0**
* **MySQL** (Banco de dados)
* **Django Bootstrap 5** (Estilização)
* **Python Dotenv** (Gerenciamento de variáveis de ambiente)

## 📋 Funcionalidades

O sistema permite realizar as seguintes operações sobre o cadastro de funcionários:

* **Listar:** Visualização de todos os funcionários cadastrados em uma tabela.
* **Detalhar:** Visualização dos dados completos de um funcionário específico.
* **Cadastrar:** Formulário para adição de novos funcionários (Nome, CPF, E-mail, Remuneração).
* **Editar:** Atualização dos dados de um funcionário existente.
* **Remover:** Exclusão de um funcionário com modal de confirmação para segurança.

## 🔧 Pré-requisitos

Antes de começar, você precisará ter instalado em sua máquina:
* [Python](https://www.python.org/)
* [MySQL](https://www.mysql.com/)
* [Git](https://git-scm.com/)

## ⚙️ Configuração e Instalação

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/joaoftonial/atividade-crud.git](https://github.com/joaoftonial/atividade-crud.git)
    cd atividade-crud
    ```

2.  **Crie e ative um ambiente virtual:**
    ```bash
    # Windows
    python -m venv venv
    venv\Scripts\activate

    # Linux/macOS
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Configure as Variáveis de Ambiente:**
    O projeto utiliza um arquivo `.env` para proteger dados sensíveis. Crie um arquivo chamado `.env` na raiz do projeto (mesmo nível do `manage.py`) e preencha com suas configurações locais:

    ```env
    SECRET_KEY=sua_chave_secreta_aqui
    DEBUG=True
    DB_NAME=nome_do_seu_banco
    DB_USER=seu_usuario_mysql
    DB_PASSWORD=sua_senha_mysql
    DB_HOST=localhost
    DB_PORT=3306
    ```
    *Nota: Certifique-se de criar o banco de dados no MySQL antes de prosseguir.*

5.  **Aplique as Migrações:**
    Isso criará as tabelas necessárias no seu banco de dados MySQL.
    ```bash
    python manage.py migrate
    ```

6.  **Execute o Servidor:**
    ```bash
    python manage.py runserver
    ```

7.  **Acesse o projeto:**
    Abra o navegador e vá para: `http://127.0.0.1:8000/app/lista_funcionarios`

## 📂 Estrutura do Projeto

* **`app/`**: Contém a lógica principal da aplicação (models, views, urls e templates).
    * **Models**: Define a estrutura do `Funcionario` (Nome, CPF, Email, Remuneração).
    * **Views**: Utiliza *Class Based Views* do Django (`CreateView`, `ListView`, `UpdateView`, etc.) para gerenciar as requisições.
    * **Templates**: Arquivos HTML estilizados com Bootstrap 5.
* **`funcionarios/`**: Configurações globais do projeto Django (`settings.py`, `urls.py`).

## Autor

joaoftonial