#  Sistema de Gestão de Biblioteca Municipal em Java

> **Trabalho de Campo da Cadeira de Introdução a Algoritmos e Programação (IAP)**  
> **Instituição:** Universidade Aberta ISCED (UnISCED)  
> **Faculdade:** Faculdade de Engenharia e Agricultura  
> **Curso:** Licenciatura em Engenharia Informática  

---

## 1.  Visão Geral do Projecto

Este projecto consiste num sistema de gestão de acervo e empréstimos para uma **Biblioteca Municipal**, desenvolvido na linguagem **Java** e operado através de consola (terminal de linha de comandos). O sistema foi concebido para automatizar tarefas de controlo de stock de livros, registo de leitores e monitorização de requisições e devoluções.
A aplicação simula uma base de dados estática em memória, utilizando **exclusivamente vetores (arrays unidimensionais) e matrizes bidimensionais**, sem o recurso a coleções dinâmicas (`ArrayList`) ou bibliotecas externas de persistência, respeitando integralmente os requisitos académicos da cadeira.

---

## 2. Funcionalidades do Sistema

* **Registo de Livros:** Cadastro de novas obras com gerador de ID automático (`L1`, `L2`, ...), título, autor, ano de publicação e quantidade em stock.
* **Registo de Utilizadores:** Cadastro dos leitores da biblioteca com atribuição sequencial de ID único (`U1`, `U2`, ...).
* **Consulta e Pesquisa no Catálogo:**
  * Listagem completa em tabela formatada na consola.
  * Pesquisa flexível por **Título** ou **Autor** (ignora maiúsculas/minúsculas e aceita termos parciais).
* **Gestão de Empréstimos e Devoluções:**
  * Validação de existência prévia do utilizador e do livro.
  * Verificação de disponibilidade de exemplares antes de efetuar a reserva.
  * Abatimento automático de quantidade no stock aquando do empréstimo.
  * Devolução automatizada com reposição de stock e atualização de estado (`DEVOLVIDO`).
* **Painel de Estatísticas:**
  * Contagem total de livros e utilizadores registados.
  * Histórico total de requisições efetuadas.
  * Identificação algorítmica do **livro mais emprestado**.

---

## 3. Arquitetura e Estruturas de Dados

Toda a gestão de dados opera exclusivamente em memória estática através de estruturas nativas do Java:

| Estrutura | Tipo | Mapeamento / Função |
| :--- | :--- | :--- |
| `livros[][]` | `String[50][5]` | `[0]` ID \| `[1]` Título \| `[2]` Autor \| `[3]` Ano \| `[4]` Quantidade em Stock |
| `utilizadores[][]` | `String[50][2]` | `[0]` ID \| `[1]` Nome Completo |
| `emprestimos[][]` | `String[100][3]`| `[0]` ID do Livro \| `[1]` ID do Utilizador \| `[2]` Estado (`"EMPRESTADO"`/`"DEVOLVIDO"`) |
| `totalEmprestimosLivro[]` | `int[50]` | Contagem acumulada de requisições por livro para cálculo do mais emprestado |

---

## 4.  Dependências e Pré-requisitos

Para configurar e executar este projecto, necessita de ter os seguintes elementos instalados no seu computador:

| Dependência | Versão Mínima | Descrição |
| :--- | :--- | :--- |
| **Java Development Kit (JDK)** | JDK 8 (ou superior, ex: 17 / 21) | Kit de desenvolvimento necessário para compilar e executar o código Java. |
| **Terminal / Prompt** | Qualquer | Bash, PowerShell, CMD ou o Terminal integrado do VS Code / IDE. |
| **Git** *(Opcional)* | 2.x+ | Utilizado para clonar o repositório. |

*Nota: O projecto não utiliza nenhuma biblioteca externa (`.jar` adicional ou frameworks como Maven/Gradle). Depende exclusivamente da biblioteca padrão do Java (`java.util.Scanner`).*

---

## 5
Aqui tens uma **descrição formal e estruturada do projecto**, ideal tanto para colocares no teu ficheiro `README.md` do GitHub como para usares na introdução ou no resumo do teu relatório escrito (Word/PDF) da UnISCED:

---

### 📝 Descrição do Projecto

#### **Título:**

**Sistema de Gestão de Biblioteca Municipal em Java**

#### **Resumo Geral:**

O **Sistema de Gestão de Biblioteca Municipal** é uma aplicação baseada em consola (interface de linha de comandos) desenvolvida na linguagem de programação **Java**. O projecto foi concebido como Trabalho de Campo para a disciplina de **Introdução a Algoritmos e Programação (IAP)** no curso de Licenciatura em Engenharia Informática da **UnISCED**.

O objectivo principal da aplicação é automatizar e simplificar a gestão operacional de uma biblioteca, permitindo o controlo do acervo bibliográfico, o registo de leitores e a gestão do fluxo de empréstimos e devoluções de obras.

---

### 🎯 Principais Objectivos e Características Técnicas

* **Manipulação de Memória Estática:** Toda a gestão de dados (livros, utilizadores e histórico de requisições) é realizada em memória utilizando exclusivamente **vetores (arrays unidimensionais) e matrizes bidimensionais**, sem o recurso a bases de dados externas ou coleções dinâmicas, atendendo aos requisitos académicos da cadeira.


* **Gestão de Acervo (Livros):** Permite o cadastro de novas obras com identificadores únicos gerados automaticamente (`L1`, `L2`, ...), registando título, autor, ano de publicação e quantidade de exemplares disponíveis.


* **Gestão de Utilizadores:** Registo de leitores/utentes da biblioteca com IDs atribuídos sequencialmente (`U1`, `U2`, ...).


* **Pesquisa e Consulta Flexível:** Disponibiliza a listagem completa do catálogo em formato tabular e permite a busca direcionada por palavras-chave no **título** ou **autor** do livro.


* **Controlo de Empréstimos e Devoluções:** Valida a existência do utilizador e do livro, verifica o stock disponível antes de efetuar a reserva e atualiza automaticamente o inventário no momento do empréstimo e da devolução.


* **Painel Informativo e Estatísticas:** Apresenta relatórios dinâmicos sobre o número total de livros e utilizadores registados, total de operações efetuadas e a identificação do **livro mais requisitado** pelo público.



---

### Ficha Técnica do Projecto

| Parâmetro | Detalhe |
| --- | --- |
| **Linguagem** | Java (JDK 8 ou superior)

 |
| **Paradigma** | Programação Estruturada / Imperativa |
| **Estrutura de Dados** | Matrizes Bidimensionais (`String[][]`) e Vetores (`int[]`)

 |
| **Interface** | Consola / Terminal de Linha de Comandos

 |
| **Autor** | António Agostinho Junior

 |
| **Instituição** | Universidade Aberta ISCED (UnISCED)

 |
| **Repositório GitHub** | [ajunior22-hub/sistema-biblioteca-java](https://github.com/ajunior22-hub/sistema-biblioteca-java)<br> |


## 5. Autor e Informações Académicas
Autor: António Agostinho Junior

Instituição: Universidade Aberta ISCED (UnISCED)

Faculdade: Faculdade de Engenharia e Agricultura

Curso: Licenciatura em Engenharia Informática

Cadeira: Introdução a Algoritmos e Programação (IAP)

Repositório GitHub: ajunior22-hub/sistema-biblioteca-java

---

## 6.  Configuração do Ambiente, Compilação e Execução

### Passo 1: Verificar se o Java está instalado
Abre o teu terminal (Prompt de Comando, PowerShell ou Terminal do Linux/Mac) e executa:
```bash
java -version
