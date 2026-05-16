Documento de Requisitos de Software (DRS) - Kan-School
1. Introdução
1.1 Visão Geral
O Kan-School é um sistema web de gerenciamento de atividades escolares baseado na metodologia Kanban. A plataforma adota uma arquitetura desacoplada, utilizando FastAPI para a construção de uma API REST robusta e o ecossistema Django restrito à área de administração de dados. A plataforma permitirá que estudantes e professores organizem tarefas acadêmicas através de quadros visuais compostos por colunas e cartões, facilitando o acompanhamento do progresso das atividades escolares.
1.2 Objetivos do Sistema
O sistema tem como objetivos:
Organizar tarefas escolares em modelo Kanban;
Melhorar a produtividade dos estudantes;
Facilitar o acompanhamento de atividades acadêmicas;
Promover colaboração entre usuários;
Aplicar conceitos de metodologias ágeis no ambiente educacional.
1.3 Público-Alvo
O sistema será utilizado por:
Estudantes;
Professores;
Grupos de estudo;
Instituições educacionais.
2. Escopo do Sistema
2.1 Escopo Incluído
O Kan-School incluirá:
Cadastro e autenticação de usuários;
Criação de quadros Kanban;
Criação e edição de tarefas;
Movimentação de tarefas entre colunas;
Definição de prazos;
Compartilhamento de quadros;
Acompanhamento visual de progresso;
Painel administrativo para gerenciamento interno.
2.2 Escopo Não Incluído
Nesta versão inicial não serão incluídos:
Aplicativo mobile nativo;
Integração com sistemas escolares oficiais;
Inteligência artificial;
Videochamadas integradas.
3. Requisitos Funcionais (RF)
RF00: O sistema deve permitir que alunos e professores criem contas com e-mail e senha.
RF01: O usuário deve poder criar múltiplos quadros (ex: um para cada disciplina).
RF02: O usuário deve poder criar, editar e excluir tarefas.
RF03: A movimentação de tarefas deve ser visual (arrastar e soltar entre colunas).
RF04: O sistema deve permitir a definição de prazos para as tarefas.
RF05: O sistema deve permitir comentários em tarefas.
RF06: O sistema deve armazenar o histórico de ações dos usuários nos quadros.
RF07: O usuário deve poder compartilhar quadros via e-mail, link público ou restrito a usuários cadastrados.
RF08: O sistema deve diferenciar permissões entre "Dono do Quadro" e "Convidado/Editor".
RF09: O sistema deve possuir interface responsiva adaptável a dispositivos móveis e desktops.
RF10: O sistema deve disponibilizar um painel administrativo web para gerenciamento de usuários e auditoria de dados.
4. Requisitos Não Funcionais (RNF)
RNF00: O sistema deve possuir uma interface intuitiva e de fácil usabilidade.
RNF01: O tempo de resposta das requisições da API deve ser inferior a 2 segundos.
RNF02: O sistema deve garantir a segurança, privacidade e integridade dos dados trafegados.
RNF03: O sistema deve utilizar autenticação segura baseada em tokens (JWT).
RNF04: O sistema deve possuir alta disponibilidade, operando no mínimo 99% do tempo.
5. Arquitetura Técnica
5.1 Estrutura do Sistema
O sistema adota um modelo estritamente desacoplado, separando completamente as responsabilidades do servidor de API e do cliente web (SPA).
5.2 Stacks Utilizadas
5.2.1 Stack Backend (API & Admin)
Tecnologias utilizadas no ecossistema de backend:
Python 3
FastAPI: Framework principal para construção da API REST, validação de dados e regras de negócio.
OAuth2 / JWT (JSON Web Tokens): Mecanismo de autenticação e autorização da API.
Django (Apenas Admin): Utilizado exclusivamente para a interface administrativa nativa (Django Admin), facilitando o gerenciamento do banco de dados por administradores do sistema.
GitHub: Plataforma para versionamento de código.
5.2.2 Stack Frontend (Single Page Application - SPA)
Interface gráfica consumidora da API:
HTML5 / CSS3 / JavaScript (ES6+)
Tailwind CSS ou Bootstrap para estilização.
Framework/Biblioteca Moderna: React (ao invés de templates de backend).
5.2.3 Banco de Dados e Persistência
PostgreSQL: Banco de dados relacional principal para o ambiente de produção.
SQLite: Utilizado apenas para facilidade no ambiente de desenvolvimento local.
SQLAlchemy: ORM utilizado pelo FastAPI para manipulação dos dados de forma assíncrona.
Alembic: Ferramenta para controle e execução de migrações do banco de dados.
6. Modelo de Dados