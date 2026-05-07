# Documento de Requisitos de Software (DRS)

## 1. Introdução

### 1.1 Visao Geral
O Kan-School é um sistema web de gerenciamento de atividades escolares baseado na metodologia Kanban, desenvolvido utilizando o framework Django.
A plataforma permitirá que estudantes e professores organizem tarefas acadêmicas através de quadros visuais compostos por colunas e cartões, facilitando o acompanhamento do progresso das atividades escolares.

### 1.2 Objetivos do Sistema
O sistema tem como objetivos:
Organizar tarefas escolares em modelo Kanban;
Melhorar a produtividade dos estudantes;
Facilitar o acompanhamento de atividades acadêmicas;
Promover colaboração entre usuários;
Aplicar conceitos de metodologias ágeis no ambiente educacional.

### 1.3 Público Alvo
O sistema será utilizado por:
Estudantes;
Professores;
Grupos de estudo;
Instituições educacionais.

## 2. Escopo do Sistema

### 2.1 Escopo Incluído
O Kan-School incluirá:
Cadastro e autenticação de usuários;
Criação de quadros Kanban;
Criação e edição de tarefas;
Movimentação de tarefas entre colunas;
Definição de prazos;
Compartilhamento de quadros;
Acompanhamento visual de progresso.

### 2.2 Escopo não incluido
Nesta versão inicial não serão incluídos:
Aplicativo mobile nativo;
Integração com sistemas escolares oficiais;
Inteligência artificial;
Videochamadas integradas.

### 3. Requisitos Funcionaís
Código
Requisito
### RF00
O sistema deve permitir que alunos e professores criem contas com e-mail e senha.### RF01
O sistema deve realizar autenticação (login/logout)
### RF01
O usuário deve poder criar múltiplos quadros (ex: um para cada disciplina)
### RF02
O usuário deve criar, editar e excluir tarefas
### RF03
A movimentação de tarefas deve ser visual (arrastar e soltar entre colunas).
### RF04
O sistema deve permitir definição de prazos
### RF05
O sistema deve permitir comentários em tarefas
### RF06
O sistema deve armazenar histórico de ações
### RF07
O usuário deve compartilhar quadros via e-mail, link público ou apenas para usuários já cadastrados.
### RF08 
Diferenciar permissões entre "Dono do Quadro" e "Convidado/Editor".

### 4. Requisitos Não Funcionais

### Código:

Requisitos -
### RNF00
O sistema deve possuir interface intuitiva
### RNF01
O sistema deve ser responsivo
### RNF02
O tempo de resposta deve ser inferior a 2 segundos
### RNF03
O sistema deve garantir segurança dos dados
### RNF04
O sistema deve utilizar autenticação segura
### RNF05
O sistema deve estar disponível 99% do tempo

### 5. Arquitetura Técnica
### 5.1 Stacks
### 5.1.1 Stack Backend
Tecnologias utilizadas no backend:
Python 3
Django
Django REST Framework (API)
Django Authentication System
JWT ou Session Authentication
GitHub (versionamento)
Monolítica (Templates)
### 5.1.2 Stack Frontend
Interface do usuário:
HTML5
CSS3
JavaScript
Bootstrap ou Tailwind CSS
Templates Django (ou React futuramente)
Desacoplada (API + SPA)
### 5.1.7 Banco de Dados
Sistema de persistência:
PostgreSQL (principal)
SQLite (ambiente de desenvolvimento)
Django ORM para manipulação dos dados.

## 6. Modelo de Dados
