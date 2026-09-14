# Portas Lógicas e a Base da Computação

## Origem e Evolução

* **Lógica Booleana:** As portas lógicas nasceram desta base matemática. A revolução aconteceu quando esses conceitos abstratos foram aplicados fisicamente na eletrônica.
* **Avanço Tecnológico:** A eletrônica digital ganhou força na década de 1950 com a popularização dos transistores e foi massivamente aprimorada nos anos 1960 com a criação dos circuitos integrados.

## Do Transistor ao Processador

A arquitetura de processamento é construída em camadas de complexidade:

* **Transistor:** A unidade fundamental. Sozinho, atua apenas como uma chave (liga/desliga).
* **Portas Lógicas:** A combinação estruturada de transistores cria portas capazes de processar sinais e executar funções lógicas específicas.
* **Circuitos Operadores:** O agrupamento de várias portas lógicas forma circuitos complexos que realizam **operações matemáticas** (soma, subtração) e **lógicas** (comparações).
* **Capacidade de Processamento:** O poder e a velocidade de um processador são diretamente determinados pela quantidade e eficiência desses circuitos operadores.

## Portas Lógicas Básicas

O fluxo de dados é binário (`1` = Ligado/Verdadeiro, `0` = Desligado/Falso).

* **NOT (Negação / Inversora):** A saída é o oposto exato da entrada. Se entra 1, sai 0. Se entra 0, sai 1.
  * Representação: `A~` ou `Ā` (A com barra horizontal em cima).
* **AND (E):** A saída será 1 **apenas se todas** as entradas forem 1. Funciona como uma condição estrita de que tudo precisa ser verdadeiro.
  * Representação: `A*B`
* **OR (Ou):** A saída será 1 se **pelo menos uma** das entradas for 1. Só resulta em 0 se absolutamente todas as entradas forem 0.
  * Representação: `A+B`
* **NAND (Não E):** A negação da porta AND. A saída só será 0 se todas as entradas forem 1. Qualquer outra combinação resulta em 1.
  * Representação: `(A*B)~`
* **NOR (Não Ou):** A negação da porta OR. A saída será 1 **apenas se todas** as entradas forem 0. Qualquer sinal de 1 na entrada zera a saída.
  * Representação: `(A+B)~`

---

## Exercício 1
<img src=imagem1.png>

| A | B | C | A\*B | A\*C | (A\*B)+(A\*C) |
|---|---|---|------|------|---------------|
| 0 | 0 | 0 | 0    | 0    | 0             |
| 0 | 0 | 1 | 0    | 0    | 0             |
| 0 | 1 | 0 | 0    | 0    | 0             |
| 0 | 1 | 1 | 0    | 0    | 0             |
| 1 | 0 | 0 | 0    | 0    | 0             |
| 1 | 0 | 1 | 0    | 1    | 1             |
| 1 | 1 | 0 | 1    | 0    | 1             |
| 1 | 1 | 1 | 1    | 1    | 1             |

| A | B | C | B+C | A\*(B+C) |
|---|---|---|-----|----------|
| 0 | 0 | 0 | 0   | 0        |
| 0 | 0 | 1 | 1   | 0        |
| 0 | 1 | 0 | 1   | 0        |
| 0 | 1 | 1 | 1   | 0        |
| 1 | 0 | 0 | 1   | 0        |
| 1 | 0 | 1 | 1   | 0        |
| 1 | 1 | 0 | 1   | 0        |
| 1 | 1 | 1 | 1   | 1        |

---

## Exercício 2
<img src=imagem2.png>

| A | B | C | A+B | (B+C)' | [(A+B).(B+C)']' | C.[(A+B).(B+C)']' | B+C | (A+B).(B+C)' |
|---|---|---|-----|--------|------------------|-------------------|-----|--------------|
| 0 | 0 | 0 | 0   | 1      | 1                | 0                 | 0   | 0            |
| 0 | 0 | 1 | 0   | 0      | 1                | 1                 | 1   | 0            |
| 0 | 1 | 0 | 1   | 0      | 1                | 0                 | 1   | 0            |
| 0 | 1 | 1 | 1   | 0      | 1                | 1                 | 1   | 0            |
| 1 | 0 | 0 | 1   | 1      | 0                | 0                 | 0   | 1            |
| 1 | 0 | 1 | 1   | 0      | 1                | 1                 | 1   | 0            |
| 1 | 1 | 0 | 1   | 0      | 1                | 0                 | 1   | 0            |
| 1 | 1 | 1 | 1   | 0      | 1                | 1                 | 1   | 0            |

---

## Exercício 3
<img src=imagem3.png>

| A | B | C | D | A\*B | C+D | ((A\*B)\*(C+D))~ | D+((A\*B)\*(C+D))~ | (A\*B)\*(C+D)  |
|---|---|---|---|------|-----|------------------|--------------------|----------------|
| 0 | 0 | 0 | 0 | 0    | 0   | 1                | 1                  | 0              |
| 0 | 0 | 0 | 1 | 0    | 1   | 1                | 1                  | 0              |
| 0 | 0 | 1 | 0 | 0    | 1   | 1                | 1                  | 0              |
| 0 | 0 | 1 | 1 | 0    | 1   | 1                | 1                  | 0              |
| 0 | 1 | 0 | 0 | 0    | 0   | 1                | 1                  | 0              |
| 0 | 1 | 0 | 1 | 0    | 1   | 1                | 1                  | 0              |
| 0 | 1 | 1 | 0 | 0    | 1   | 1                | 1                  | 0              |
| 0 | 1 | 1 | 1 | 0    | 1   | 1                | 1                  | 0              |
| 1 | 0 | 0 | 0 | 0    | 0   | 1                | 1                  | 0              |
| 1 | 0 | 0 | 1 | 0    | 1   | 1                | 1                  | 0              |
| 1 | 0 | 1 | 0 | 0    | 1   | 1                | 1                  | 0              |
| 1 | 0 | 1 | 1 | 0    | 1   | 1                | 1                  | 0              |
| 1 | 1 | 0 | 0 | 1    | 0   | 1                | 1                  | 0              |
| 1 | 1 | 0 | 1 | 1    | 1   | 0                | 1                  | 1              |
| 1 | 1 | 1 | 0 | 1    | 1   | 0                | 0                  | 1              |
| 1 | 1 | 1 | 1 | 1    | 1   | 0                | 1                  | 1              |

## Exercício 4
<img src=imagem4.png>

| A | B | C | D | A*B | ((A*B)*D)' | (C+D)' | A+(C+D)' | ((A*B)*D)'+[A+(C+D)'] | (A*B)*D |
|---|---|---|---|-----|------------|--------|----------|------------------------|---------|
| 0 | 0 | 0 | 0 | 0   | 1          | 1      | 1        | 1                      | 0       |
| 0 | 0 | 0 | 1 | 0   | 1          | 0      | 0        | 1                      | 0       |
| 0 | 0 | 1 | 0 | 0   | 1          | 0      | 0        | 1                      | 0       |
| 0 | 0 | 1 | 1 | 0   | 1          | 0      | 0        | 1                      | 0       |
| 0 | 1 | 0 | 0 | 0   | 1          | 1      | 1        | 1                      | 0       |
| 0 | 1 | 0 | 1 | 0   | 1          | 0      | 0        | 1                      | 0       |
| 0 | 1 | 1 | 0 | 0   | 1          | 0      | 0        | 1                      | 0       |
| 0 | 1 | 1 | 1 | 0   | 1          | 0      | 0        | 1                      | 0       |
| 1 | 0 | 0 | 0 | 0   | 1          | 1      | 1        | 1                      | 0       |
| 1 | 0 | 0 | 1 | 0   | 1          | 0      | 1        | 1                      | 0       |
| 1 | 0 | 1 | 0 | 0   | 1          | 0      | 1        | 1                      | 0       |
| 1 | 0 | 1 | 1 | 0   | 1          | 0      | 1        | 1                      | 0       |
| 1 | 1 | 0 | 0 | 1   | 1          | 1      | 1        | 1                      | 0       |
| 1 | 1 | 0 | 1 | 1   | 0          | 0      | 1        | 1                      | 1       |
| 1 | 1 | 1 | 0 | 1   | 1          | 0      | 1        | 1                      | 0       |
| 1 | 1 | 1 | 1 | 1   | 0          | 0      | 1        | 1                      | 1       |

## Exercício 5
<img src=imagem5.png>

| A | B | C | D | A+B | (C*D)' | (A+B)+(C*D)' | (A*C)' | (A.C)'.((A+B)+(C.D)') | A*C |
|---|---|---|---|-----|--------|--------------|--------|----------------------|-----|
| 0 | 0 | 0 | 0 | 0   | 1      | 1            | 1      | 1                    | 0   |
| 0 | 0 | 0 | 1 | 0   | 1      | 1            | 1      | 1                    | 0   |
| 0 | 0 | 1 | 0 | 0   | 1      | 1            | 1      | 1                    | 0   |
| 0 | 0 | 1 | 1 | 0   | 0      | 0            | 1      | 0                    | 0   |
| 0 | 1 | 0 | 0 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 0 | 1 | 0 | 1 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 0 | 1 | 1 | 0 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 0 | 1 | 1 | 1 | 1   | 0      | 1            | 1      | 1                    | 0   |
| 1 | 0 | 0 | 0 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 1 | 0 | 0 | 1 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 1 | 0 | 1 | 0 | 1   | 1      | 1            | 0      | 0                    | 1   |
| 1 | 0 | 1 | 1 | 1   | 0      | 1            | 0      | 0                    | 1   |
| 1 | 1 | 0 | 0 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 1 | 1 | 0 | 1 | 1   | 1      | 1            | 1      | 1                    | 0   |
| 1 | 1 | 1 | 0 | 1   | 1      | 1            | 0      | 0                    | 1   |
| 1 | 1 | 1 | 1 | 1   | 0      | 1            | 0      | 0                    | 1   |

<img src=imagem6.png>
<img src=imagem6resolvida.png>
