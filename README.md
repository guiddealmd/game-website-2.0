# 🎮 Game Website 2.0

[![Status](https://img.shields.io/badge/status-concluído-brightgreen)]()  
[![PHP](https://img.shields.io/badge/PHP-8.x-blue?logo=php)]()  
[![License](https://img.shields.io/badge/license-MIT-green)]()

Um website de jogos desenvolvido com **PHP, MySQL, HTML, CSS e JavaScript**, estruturado em um padrão próximo ao **MVC** (Model-View-Controller).  
O sistema foi concluído com foco em oferecer cadastro e autenticação de usuários, gerenciamento de produtos e carrinho de compras, funcionando como um modelo de e-commerce voltado ao universo gamer.

---

## 📑 Índice

1. [Tecnologias](#-tecnologias)  
2. [Estrutura de Diretórios](#-estrutura-de-diretórios)  
3. [Instalação](#-instalação)  
4. [Fluxo do Projeto (MVC)](#-fluxo-do-projeto-mvc)  
5. [Funcionalidades](#-funcionalidades)  
6. [Licença](#-licença)  
7. [Contato](#-contato)  

---

## 🧰 Tecnologias

- **Backend:** PHP 8.x  
- **Banco de Dados:** MySQL  
- **Frontend:** HTML5, CSS3, JavaScript  
- **Servidor Local:** XAMPP / WAMP / MAMP  
- **Organização:** Padrão MVC simplificado  

---

## 📁 Estrutura de Diretórios

```

game-website-2.0/
│
├── public/                     # Arquivos acessíveis pelo navegador
│   ├── index.php                # Página inicial
│   ├── login.php                # Login
│   ├── logout.php               # Logout
│   ├── cadastro.php             # Registro
│   ├── produtos.php             # Listagem de produtos
│   ├── carrinho.php             # Carrinho de compras
│   └── assets/                  # Arquivos públicos (CSS, JS, imagens)
│
├── src/                        # Código-fonte principal
│   ├── Controllers/             # Controladores
│   │   ├── UserController.php
│   │   ├── ProductController.php
│   │   └── CartController.php
│   │
│   ├── Models/                  # Modelos de entidades
│   │   ├── User.php
│   │   ├── Product.php
│   │   └── Cart.php
│   │
│   ├── Database/                # Conexão e queries
│   │   └── db.php
│   │
│   └── Helpers/                 # Funções auxiliares
│       └── auth.php
│
├── views/                      # Templates (HTML + PHP)
│   ├── layouts/                 # Estruturas globais
│   │   ├── header.php
│   │   ├── footer.php
│   │   └── navbar.php
│   │
│   ├── auth/                    # Telas de login/cadastro
│   │   ├── login.php
│   │   └── register.php
│   │
│   ├── products/                # Telas de produtos
│   │   ├── list.php
│   │   └── edit.php
│   │
│   └── cart/                    # Tela do carrinho
│       └── index.php
│
├── config/                     # Configurações do projeto
│   ├── config.php               # Variáveis globais
│   └── routes.php               # Mapeamento de rotas (opcional)
│
├── tests/                      # Testes automatizados
│   └── UserTest.php
│
├── .gitignore
├── composer.json
├── LICENSE
└── README.md

````

---

## 🔄 Fluxo do Projeto (MVC)

1. O usuário acessa uma rota pública em `public/` (ex.: `login.php`).  
2. Essa rota aciona o **Controller** (ex.: `UserController`).  
3. O Controller interage com o **Model** (ex.: `User.php`) para consultar o banco.  
4. Os dados são enviados para a **View** (ex.: `views/auth/login.php`).  
5. A View renderiza o HTML final para o usuário.  

---

## 🚀 Instalação

### 1. Clone o repositório
```bash
git clone https://github.com/guiddealmd/game-website-2.0.git
````

### 2. Configure o ambiente

* Instale XAMPP, WAMP ou similar.
* Certifique-se que **PHP e MySQL** estão ativos.

### 3. Banco de dados

* Crie o banco:

  ```sql
  CREATE DATABASE game_website;
  ```
* Configure as credenciais em `src/Database/db.php`:

  ```php
  $host = "localhost";
  $usuario = "root";
  $senha = "";
  $dbname = "game_website";
  ```

### 4. Execute o projeto

* Coloque a pasta em `htdocs` (ou equivalente).
* Abra no navegador:

  ```
  http://localhost/game-website-2.0/public/
  ```

---

## ✅ Funcionalidades

* 👤 Cadastro e autenticação de usuários
* 🔑 Login/logout com controle de sessão
* 🔒 Alteração de senha
* 📦 Cadastro e listagem de produtos
* 🛒 Carrinho de compras (adicionar, atualizar, remover)
* 🛠 Painel de administração para CRUD de usuários e produtos

---

## 📄 Licença

Este projeto está sob a licença **MIT**.
Veja o arquivo [LICENSE](LICENSE) para mais informações.
