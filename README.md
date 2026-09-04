
# Sistema de Gestão de Biblioteca Municipal em Java

> Trabalho de Campo da disciplina de **Introdução a Algoritmos e Programação (IAP)**  
> **Instituição:** Universidade Aberta ISCED (UnISCED)  
> **Faculdade:** Faculdade de Engenharia e Agricultura  
> **Curso:** Licenciatura em Engenharia Informática  

---

##  1. Visão Geral do Projecto

Este projecto consiste num sistema de gestão de acervo e empréstimos para uma Biblioteca Municipal e desenvolvido em **Java** e operado via **consola (terminal)**. O sistema foi concebido para automatizar tarefas de controlo de stock de livros, registo de leitores e monitorização de requisições e devoluções.
A aplicação simula uma **base de dados estática em memória**, utilizando exclusivamente **vetores (arrays unidimensionais)** e **matrizes bidimensionais**, sem o recurso a coleções dinâmicas ou bibliotecas externas de persistência, respeitando os requisitos da cadeira.

---

## 2. Funcionalidades do Sistema

- [x] **Registo de Livros:** Cadastro de novas obras com gerador de ID automático (`L1`, `L2`, ...), título, autor, ano de publicação e quantidade em stock.
- [x] **Registo de Utilizadores:** Cadastro dos leitores da biblioteca com ID único (`U1`, `U2`, ...).
- [x] **Consulta e Pesquisa no Catálogo:**
  - Listagem completa em tabela formatada na consola.
  - Pesquisa flexível por **Título** ou **Autor** (ignora maiúsculas/minúsculas e aceita termos parciais).
- [x] **Gestão de Empréstimos e Devoluções:**
  - Validação de existência do utilizador e do livro.
  - Verificação de disponibilidade de exemplares antes de efetuar a reserva.
  - Abatimento automático de quantidade no stock aquando do empréstimo.
  - Devolução automatizada com reposição de stock e atualização de estado (`DEVOLVIDO`).
- [x] **Painel de Estatísticas:**
  - Contagem total de livros e utilizadores registados.
  - Histórico total de requisições.
  - Identificação algorítmica do **livro mais emprestado**.

---

## 3. Dependências e Pré-requisitos

Para configurar e executar este projecto, necessita de ter os seguintes elementos instalados no seu computador:

| Dependência | Versão Mínima | Descrição |
| :--- | :--- | :--- |
| **Java Development Kit (JDK)** | **JDK 8** (ou superior, ex: JDK 17 / 21) | Kit de desenvolvimento necessário para compilar e executar o código Java. |
| **Terminal / Prompt** | Qualquer | Bash, PowerShell, CMD ou o Terminal integrado do VS Code / IDE. |
| **Git** *(Opcional)* | 2.x+ | Utilizado para clonar o repositório. |

> **Nota:** O projecto não utiliza nenhuma biblioteca externa (`.jar` adicional ou frameworks como Maven/Gradle). Depende exclusivamente da biblioteca padrão do Java (`java.util.Scanner`).

---

## 4. Configuração do Ambiente

### Passo 1: Verificar se o Java está instalado
Abre o teu terminal (Prompt de Comando, PowerShell ou Terminal do Linux/Mac) e executa o seguinte comando:

## Como Compilar e Executar

**Clonar este repositório:**
   ```bash
   git clone [https://github.com/ajunior22-hub/sistema-biblioteca-java.git](https://github.com/ajunior22-hub/sistema-biblioteca-java.git)
