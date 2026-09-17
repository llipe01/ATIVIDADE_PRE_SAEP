🗳️ Sistema de Eleição — CRUD em PHP

📚 Projeto de treino/estudo desenvolvido para a prova SAEP (Sistema de Avaliação da Educação Profissional).

Aplicação web simples que implementa um CRUD completo (Criar, Ler, Atualizar e Excluir) em PHP + MySQL, simulando um cadastro de Eleitores e Candidatos.

🎯 Objetivo

Este repositório foi criado como material de prática para a prova SAEP, com foco em demonstrar o domínio dos seguintes conceitos:

Lógica de programação aplicada a operações CRUD
Conexão de PHP com banco de dados MySQL usando PDO
Uso de prepared statements (proteção contra SQL Injection)
Sanitização de dados de entrada e saída (proteção contra XSS)
Estruturação de um projeto web em camadas simples (conexão, regras, views)
Boas práticas básicas de formulários, validação e redirecionamento HTTP
🛠️ Tecnologias utilizadas
PHP (puro, sem framework)
MySQL / MariaDB
PDO para acesso ao banco de dados
HTML5 e CSS3
🗃️ Estrutura do banco de dados

O sistema trabalha com duas tabelas:

eleitor

Campo	Tipo	Descrição
id_eleitor	INT (PK, auto increment)	Identificador do eleitor
nome	VARCHAR	Nome do eleitor
numero_titulo	VARCHAR	Número do título de eleitor
cidade	VARCHAR	Cidade do eleitor

candidato

Campo	Tipo	Descrição
id_candidato	INT (PK, auto increment)	Identificador do candidato
nome	VARCHAR	Nome do candidato
numero_candidato	VARCHAR	Número do candidato
cargo	VARCHAR	Cargo pleiteado
partido_ficticio	VARCHAR	Partido (fictício, apenas para fins didáticos)

O script de criação das tabelas está em schema.sql.

📂 Estrutura do projeto
crud-eleicao/
├── index.php              # Lista/consulta eleitores (página inicial)
├── eleitor_criar.php       # Inserir eleitor
├── eleitor_editar.php      # Atualizar eleitor
├── eleitor_excluir.php     # Excluir eleitor
├── candidatos.php          # Lista/consulta candidatos
├── candidato_criar.php     # Inserir candidato
├── candidato_editar.php    # Atualizar candidato
├── candidato_excluir.php   # Excluir candidato
├── db.php                  # Conexão com o banco (MySQL via PDO)
├── functions.php           # Funções auxiliares (sanitização, redirecionamento)
├── schema.sql               # Script de criação das tabelas + dados de exemplo
├── css/style.css            # Estilo visual
└── README.md
🚀 Como executar o projeto
Pré-requisitos
PHP 7.4 ou superior (com extensão pdo_mysql)
MySQL ou MariaDB (pode usar XAMPP, WAMP, Laragon, etc.)
Passo a passo
Clone o repositório
bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
Crie o banco de dados importando o script schema.sql no MySQL (via phpMyAdmin ou terminal):
bash
   mysql -u root -p < schema.sql
Configure a conexão no arquivo db.php com os dados do seu ambiente:
php
   $host   = 'localhost';
   $dbname = 'eleicao';
   $user   = 'root';
   $pass   = '';
Suba o servidor embutido do PHP:
bash
   php -S localhost:8000
Acesse no navegador:
   http://localhost:8000
✅ Funcionalidades
 Inserir novo eleitor / candidato
 Listar e consultar (com busca por nome, número, cidade, cargo ou partido)
 Atualizar dados existentes
 Excluir registros com confirmação
 Validação de campos obrigatórios
 Verificação de número duplicado (título/candidato)
⚠️ Observação

Este projeto tem fins exclusivamente educacionais, desenvolvido como treino para a prova SAEP. Os dados (candidatos, partidos e eleitores) são fictícios e não representam nenhuma eleição real.

👤 Autor

Feito por Fellipe Guarantani de Olivaeira como parte dos estudos para a prova SAEP.
