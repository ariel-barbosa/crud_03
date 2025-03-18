# Gerenciamento de Dados - CRUD

## 📌 Introdução

Este projeto é um aplicativo CRUD (Criar, Ler, Atualizar, Deletar) para gerenciamento de dados. Ele serve como uma base prática para iniciantes no desenvolvimento de software e banco de dados, permitindo a aplicação de conceitos fundamentais em um cenário real.

## 📂 Modelo de Banco de Dados

O banco de dados relacional contém três entidades principais:

### 📋 Clientes:
- `id` (chave primária, inteiro)
- `nome` (texto)
- `email` (texto)
- `telefone` (texto)

### 📦 Produtos:
- `id` (chave primária, inteiro)
- `nome` (texto)
- `descricao` (texto)
- `preco` (decimal)

### 📑 Pedidos:
- `id` (chave primária, inteiro)
- `id_cliente` (chave estrangeira, referenciando `Clientes.id`)
- `id_produto` (chave estrangeira, referenciando `Produtos.id`)
- `data_pedido` (data)

### 🛠 Script SQL:
```sql
CREATE TABLE Clientes (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    nome TEXT,
    email TEXT,
    telefone TEXT
);

CREATE TABLE Produtos (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    nome TEXT,
    descricao TEXT,
    preco REAL
);

CREATE TABLE Pedidos (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    id_cliente INTEGER,
    id_produto INTEGER,
    data_pedido DATE,
    FOREIGN KEY (id_cliente) REFERENCES Clientes(id),
    FOREIGN KEY (id_produto) REFERENCES Produtos(id)
);
```

## 🔄 Funcionalidades do CRUD

- **Criar (Create):** Adicionar novos registros.
- **Ler (Read):** Visualizar registros existentes.
- **Atualizar (Update):** Modificar dados existentes.
- **Deletar (Delete):** Remover registros do banco de dados.

## 🎨 Interface do Usuário (UI)

A interface foi desenvolvida com **HTML, CSS e JavaScript**, oferecendo:
- 📄 Listagem de registros.
- 📝 Formulários para adição e edição.
- 🗑️ Botões para exclusão.
- 🔎 Campos de pesquisa para filtragem.

## 🔗 Conexão com o Banco de Dados

- Utiliza a biblioteca adequada (ex: `sqlite3` para Python e SQLite).
- Implementa a lógica de conexão, execução de consultas e manipulação de dados.

## 🚀 Instruções de Instalação e Execução

### 🔧 Instalação:
1. Instale a linguagem de programação escolhida (Python, Java, etc.).
2. Instale bibliotecas e frameworks necessários (Flask, Django, etc.).
3. Instale o SGBD (SQLite, MySQL, etc.).

### 📂 Criação do Banco de Dados:
Execute o script SQL fornecido para criar as tabelas.

### ▶️ Execução do Aplicativo:
1. Execute o arquivo principal (`app.py` ou equivalente).
2. Acesse a interface via navegador web.

## 📁 Estrutura do Projeto

```
📂 projeto-crud
 ├── 📜 database.sql   # Script SQL para o banco de dados
 ├── 📜 app.py        # Código principal do aplicativo
 ├── 📂 templates/    # Arquivos HTML da interface
```

## 🔍 Considerações Finais

Este projeto fornece uma base para desenvolvimento de aplicativos CRUD. Ele pode ser expandido com funcionalidades como:
✅ Autenticação de usuários.
✅ Validação de dados.
✅ Geração de relatórios.

💡 **Sinta-se à vontade para contribuir e aprimorar!**
