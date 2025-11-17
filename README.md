# Documentação do Projeto - Instituto Padre Olavo

Bem-vindo à documentação do projeto de Trabalho Interdisciplinar do Instituto Padre Olavo. Este repositório contém artefatos de design e arquitetura do sistema, incluindo um conjunto abrangente de diagramas UML que descrevem seus diferentes aspectos funcionais e estruturais.

## Sobre o Projeto

Este projeto consiste em um sistema multifacetado que inclui gerenciamento de **Biblioteca**, um sistema de **Rifas** e um módulo de **Doações**. A arquitetura segue o padrão MVC (Model-View-Controller) e é composta por várias APIs que se comunicam com um banco de dados PostgreSQL.

## Diagramas UML

Abaixo está uma visão geral dos diagramas disponíveis, agrupados por tipo, para ajudar a entender o sistema.

---

### 1. Diagramas de Casos de Uso

Esses diagramas descrevem as interações entre os atores (usuários) e o sistema, mostrando as funcionalidades que cada um pode realizar.

* **UC1 - Bibliotecária (`uc1.puml`)**: Mostra as ações da Bibliotecária, como "Gerenciar livros", "Gerenciar empréstimos", "Gerenciar leitores" e "Gerenciar exemplares".
* **UC2 - Comprador (`uc2.puml`)**: Foca nas ações do Comprador de Rifa, incluindo "Buscar ingressos disponíveis", "Selecionar ingressos" e "Realizar pagamento".
* **UC3 - Administrador (`uc3.puml`)**: Detalha as responsabilidades do Administrador, como "Gerenciar usuários", "Gerenciar doações", "Gerenciar rifas" e "Gerar relatórios".

---

### 2. Diagramas de Classes

Estes diagramas detalham a estrutura estática do sistema, mostrando as classes, seus atributos, métodos e os relacionamentos entre elas.

* **Biblioteca (`biblioteca.puml`)**: Apresenta as classes principais do módulo de biblioteca, como `Livro`, `Exemplar`, `Emprestimo`, `LivroController` e `LivroService`.
* **Rifa (`rifa.puml`)**: Descreve as classes do módulo de rifa, incluindo `Rifa`, `Bilhete`, `RifaController` e `BilheteService`.
* **Doação (`doacao.puml`)**: Mostra a estrutura do módulo de doação, com classes como `Doacao`, `DoacaoController` e `DoacaoService`.

---

### 3. Diagramas de Sequência

Diagramas de sequência ilustram a ordem temporal das interações entre objetos para realizar um cenário específico.

* **Criar Livro (`criar-livro.puml`)**: Detalha o fluxo de interação desde a `Bibliotecária` até o `LivroController`, `LivroService`, `Livro` e, finalmente, o `BibliotecaDB` para criar um novo livro.
* **Renovação de Empréstimo (`renovacao-emprestimo.puml`)**: Mostra o processo de renovação, envolvendo a `Bibliotecária`, `EmprestimoController`, `EmprestimoService` e o banco de dados.
* **Selecionar Ingressos (`selecionar-ingressos.puml`)**: Descreve a sequência de eventos quando um `Usuário` seleciona um ingresso, passando pelo `BilheteController`, `BilheteService` e `RifaDB`.

---

### 4. Diagramas de Estado

Estes diagramas modelam o ciclo de vida dos objetos mais importantes do sistema, mostrando os diferentes estados pelos quais eles podem passar e as transições entre esses estados.

* **Biblioteca (`biblioteca.puml`)**: Descreve os estados de um livro, como "Livro Disponível", "Livro Emprestado", "Livro Atrasado" e "Livro Reservado".
* **Rifa (`rifa.puml`)**: Modela o ciclo de vida de uma rifa e seus bilhetes, incluindo estados como "Rifa Criada", "Bilhete Disponível", "Bilhete Reservado", "Bilhete Vendido" e "Rifa Sorteada".
* **Doação (`doacao.puml`)**: Apresenta os estados simplificados de uma doação: "Doação Iniciada", "Doação Processada" e "Doação Concluída".

---

### 5. Diagramas de Arquitetura e Componentes

Esses diagramas fornecem uma visão de alto nível da organização do sistema.

* **Arquitetura (`arquitetura.puml`)**: Ilustra a arquitetura MVC do sistema, mostrando a separação em camadas de Apresentação (View), Controlador (Controller), Serviço (Service) e Repositório (Repository), e como elas interagem com o banco de dados PostgreSQL.
* **Componentes (`componentes.puml`)**: Mostra os principais componentes de software do sistema, como `biblioteca-api`, `rifa-api`, `doacao-api`, `pagamento-api` e o `cliente-web`, e como eles se conectam ao banco de dados.

---

### 6. Modelo de Dados

* **Modelo de Dados (`dados.puml`)**: Este arquivo destina-se a conter o diagrama entidade-relacionamento (DER) ou um diagrama de classes focado nos dados, mostrando a estrutura do banco de dados. 
