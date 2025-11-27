
# 🏙️ Cidade Educação: Banco de Dados para Gestão Acadêmica

Um sistema robusto de banco de dados relacional projetado para o gerenciamento centralizado de instituições de ensino, infraestrutura acadêmica, corpo docente e discente em um contexto de "Cidade Inteligente".

-----

## 📝 Descrição Geral

O projeto **Cidade Educação** visa resolver a fragmentação de dados em ambientes educacionais municipais ou privados. O sistema permite o cadastro e controle de múltiplas instituições, cursos, disciplinas e a alocação de recursos físicos (salas e laboratórios), além de gerenciar todo o ciclo de vida das pessoas envolvidas (alunos, professores e funcionários) através de um modelo de generalização/especialização.

### Principais Funcionalidades

  * **Gestão de Pessoas:** Cadastro unificado com especialização para Alunos, Professores e Funcionários.
  * **Infraestrutura:** Controle de salas, capacidades e tipos (Laboratórios, Salas de Aula).
  * **Acadêmico:** Histórico escolar, frequência, notas e grade curricular.
  * **Logística:** Associação entre Turmas, Salas, Disciplinas e Professores.

-----

## 📐 Modelagem do Sistema

O projeto foi desenvolvido seguindo as três etapas de modelagem de dados:

### Modelo Conceitual

Diagrama Entidade-Relacionamento (DER) detalhando as entidades e suas cardinalidades.

### Modelo Lógico

A estrutura normalizada das tabelas e relacionamentos:

```text
pessoa(cod_pessoa, cod_instituicao FK, nome, email, data_nascimento, ...)
professor(cod_pessoa FK, departamento, titulação)
aluno(cod_pessoa FK, cod_turma FK, historico_escolar)
instituicao(cod_instituicao, nome, email, endereco...)
turma(cod_turma, capacidade, nome, data, horário)
... (ver arquivo Projeto logico.txt para lista completa)
```

-----

## 🗃️ Estrutura do Banco de Dados

O banco de dados utiliza um **Schema** próprio chamado `Cidade_Educacao` para organização. Abaixo estão as principais tabelas:

| Tabela | Descrição |
| :--- | :--- |
| `instituicao` | Entidade raiz, armazena dados das unidades de ensino. |
| `pessoa` | Tabela pai que armazena dados comuns (Nome, CPF, Endereço). |
| `aluno` | Especialização de Pessoa, vinculada a turmas. |
| `professor` | Especialização de Pessoa, com titulação e departamento. |
| `curso` | Cursos ofertados (ex: Medicina, ADS). |
| `turma` | Instância de oferta de disciplinas. |
| `historico_escolar` | Registro de desempenho acadêmico. |

-----

## 📖 Dicionário de Dados

A documentação completa dos metadados encontra-se no arquivo `Dicionario de Dados.pdf`. Abaixo, um exemplo da estrutura da tabela `sala`:

  * **cod\_sala (PK):** Inteiro - Identificador único da sala.
  * **cod\_tipo (FK):** Inteiro - Referência ao tipo de sala (ex: Lab de Saúde).
  * **capacidade:** Inteiro - Quantidade máxima de alunos.
  * **localizacao:** Varchar(50) - Bloco ou setor onde a sala se encontra.

-----

## 🚀 Instalação e Execução

### Pré-requisitos

  * Um SGBD compatível com SQL padrão (Recomendado: **PostgreSQL**).
  * Uma ferramenta cliente (DBeaver, pgAdmin, VS Code).

### Passo a Passo

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/seu-usuario/cidade-educacao.git
    cd cidade-educacao
    ```

2.  **Abra o arquivo SQL:**
    Localize o arquivo `Cidade_Educacao_ModeloFisico.sql`.

3.  **Execute o Script:**
    Rode o script no seu gerenciador de banco de dados. Ele irá:

      * Criar o schema `Cidade_Educacao`.
      * Criar todas as tabelas e relacionamentos.
      * Inserir dados fictícios (seed data) para teste.

-----

## 💡 Exemplos de Uso (Queries)

Aqui estão alguns exemplos de como extrair informações do banco de dados:

**1. Listar todos os Alunos e suas respectivas Turmas:**

```sql
SELECT 
    p.nome AS Aluno, 
    t.nome AS Turma 
FROM Cidade_Educacao.pessoa p
JOIN Cidade_Educacao.aluno a ON p.cod_pessoa = a.cod_pessoa
JOIN Cidade_Educacao.turma t ON a.cod_turma = t.cod_turma;
```

**2. Verificar a capacidade das salas e seus tipos:**

```sql
SELECT 
    s.nome AS Sala, 
    s.capacidade, 
    tp.nome AS Tipo 
FROM Cidade_Educacao.sala s
JOIN Cidade_Educacao.tipo tp ON s.cod_tipo = tp.cod_tipo;
```

**3. Consultar Histórico Escolar de um aluno específico:**

```sql
SELECT 
    p.nome, 
    h.nota, 
    h.situacao 
FROM Cidade_Educacao.historico_escolar h
JOIN Cidade_Educacao.pessoa p ON h.cod_pessoa = p.cod_pessoa
WHERE p.nome = 'Marcos';
```

-----

## 🛠️ Tecnologias Utilizadas

  * **Linguagem SQL:** Para estruturação (DDL) e manipulação (DML) dos dados.
  * **brModelo:** Utilizado para a criação do Modelo Conceitual e Lógico.
  * **PostgreSQL:** Banco de dados relacional alvo (compatível).

-----

## 📂 Estrutura do Repositório

```
/
├── Modelo_Fisico.sql                 # Script principal de criação e população
├── Dicionario de Dados.pdf           # Documentação técnica dos campos
├── Modelo Conceitual.brM3            # Arquivo editável do brModelo
├── Projeto logico.txt                # Esquema lógico textual
└── imagens/                          # Diagramas e prints do projeto
```
