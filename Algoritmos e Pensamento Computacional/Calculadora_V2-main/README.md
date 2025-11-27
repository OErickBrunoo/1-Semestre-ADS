
# Calculadora Científica em C

Uma calculadora científica completa desenvolvida em **C**, contendo operações matemáticas básicas, avançadas, trigonométricas, matriciais e recursos extras como histórico de operações salvo automaticamente em arquivo `.csv`.

---

## Descrição Geral

Este projeto consiste em uma calculadora científica interativa construída em linguagem C, com foco no uso de funções matemáticas, modularização de operações, manipulação de memória dinâmica, leitura de matrizes, trigonometria, equações e gerenciamento de histórico.

O objetivo principal é fornecer uma ferramenta funcional em modo console, demonstrando domínio sobre:

* Estruturas (`struct`)
* Funções matemáticas (básicas e científicas)
* Manipulação de arquivos (`.csv`)
* Loops e condicionais
* Alocação dinâmica com `malloc`
* Matrizes 3x3
* Organização modular de código em C

O programa apresenta todas as operações em um menu interativo e salva automaticamente cada operação realizada no arquivo `historico.csv`.

---

## Principais Funcionalidades

### Operações Básicas

* Adição (com múltiplos valores)
* Subtração com valor inicial
* Multiplicação (com múltiplos valores)
* Divisão
* Módulo (resto da divisão)

### Operações Avançadas

* Exponenciação
* Porcentagem
* Hipotenusa
* Raiz quadrada e cúbica
* Fatorial
* Bhaskara (equação de 2º grau)
* Teorema de Pitágoras

### Trigonometria

* Seno
* Cosseno
* Tangente
* Arcseno
* Arccosseno
* Arctangente
* Conversão graus ↔ radianos

### Operações com Matrizes 3x3

* Soma de matrizes
* Multiplicação de matrizes

### Gerenciamento de Histórico

* Histórico salvo em `historico.csv`
* Histórico carregado automaticamente ao iniciar
* Função para exibir operações realizadas
* IDs automáticos para cada operação

---

## Estrutura do Projeto

```
calculadora-cientifica
 ├── calculadora.c      # Código principal com todas as funções
 ├── historico.csv      # Gerado e atualizado automaticamente
 └── README.md          # Documentação do projeto
```

---

## Como Executar o Programa

### 1. Compilar o código

```bash
gcc calculadora.c -o calculadora -lm
```

### 2. Executar

```bash
./calculadora
```

---

## Menu de Operações

O programa apresenta o seguinte menu ao usuário:

```
[ 1] Adicao            [ 2] Subtracao            [ 3] Multiplicacao
[ 4] Divisao           [ 5] Exponenciacao        [ 6] Resto
[ 7] Porcentagem       [ 8] Hipotenusa           [ 9] Raiz Quadrada
[10] Raiz Cubica       [11] Seno                 [12] Cosseno
[13] Tangente          [14] Arcseno              [15] Arccosseno
[16] Arctangente       [17] Logaritmo base 10    [18] Logaritmo Natural
[19] Fatorial          [20] Radianos para Graus  [21] Arredondar p Baixo
[22] Arredondar p Cima [23] Graus para Radianos  [24] Teorema de Pitagoras
[25] Bhaskara          [26] Soma de Matrizes(3x3)[27] Mult. de Matrizes(3x3)

[0] Histórico
```

---

## Histórico de Operações

Cada operação realizada é registrada em:

```
historico.csv
```

Formato salvo:

```
ID, Tipo, Numero1, Numero2, Resultado
```

Ao abrir o programa, o arquivo é lido novamente para restaurar o histórico.

---

## Tecnologias Utilizadas

* Linguagem C
* stdio.h
* math.h
* stdlib.h
* string.h
* Manipulação de arquivos
* Alocação dinâmica
* Matrizes

---

## Exemplo de Execução

```
Digite o número da operação desejada: 1
Digite o total de números a somar: 3
Elemento 1: 10
Elemento 2: 20
Elemento 3: 30

Resultado: 60
```

---

## Contribuições

Sinta-se à vontade para sugerir melhorias ou enviar pull requests.

---

## Licença

Este projeto pode ser utilizado livremente para fins acadêmicos e didáticos.


