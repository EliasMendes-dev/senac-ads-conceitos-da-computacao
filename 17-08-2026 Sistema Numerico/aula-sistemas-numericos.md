# Sistemas Numéricos — Resumo da Aula

## Por que os computadores usam binário?

Tudo começa com **válvulas** e depois **transistores** — componentes que só têm dois estados possíveis:

- Conduzindo / Não conduzindo
- Ligado / Desligado (On / Off)
- Verdadeiro / Falso
- **1 / 0**

Como um transistor só consegue representar dois estados, o jeito mais natural de "falar" com um computador é usando um sistema numérico de base 2: o **binário**.

## George Boole e a lógica booleana

**George Boole** criou a lógica booleana, um sistema matemático baseado em apenas dois valores (verdadeiro/falso, 1/0). Essa lógica é a base de todo o funcionamento dos circuitos digitais: cada transistor "decide" entre conduzir ou não conduzir, o que mapeia perfeitamente para 0 e 1.

**Herman Hollerith** também é citado como figura histórica ligada à representação binária de dados (usada em seus sistemas de tabulação com cartões perfurados).

## Bases numéricas

| Sistema | Base | Símbolos usados |
|---|---|---|
| Binário | 2 | 0, 1 |
| Octal | 8 | 0, 1, 2, 3, 4, 5, 6, 7 |
| Decimal | 10 | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 |
| Hexadecimal | 16 | 0-9, A, B, C, D, E, F |
| Base64 | 64 | A-Z, a-z, 0-9, +, / |

Octal, hexadecimal e Base64 são todos **sistemas de numeração posicional**, assim como o decimal.

## Tabela de conversão

### Decimal ↔ Binário ↔ Octal

| Decimal | Binário | Octal |
|---|---|---|
| 0 | 000 | 0 |
| 1 | 001 | 1 |
| 2 | 010 | 2 |
| 3 | 011 | 3 |
| 4 | 100 | 4 |
| 5 | 101 | 5 |
| 6 | 110 | 6 |
| 7 | 111 | 7 |

### Decimal ↔ Binário ↔ Hexadecimal

| Decimal | Binário | Hexadecimal |
|---|---|---|
| 0 | 0000 | 0 |
| 1 | 0001 | 1 |
| 2 | 0010 | 2 |
| 3 | 0011 | 3 |
| 4 | 0100 | 4 |
| 5 | 0101 | 5 |
| 6 | 0110 | 6 |
| 7 | 0111 | 7 |
| 8 | 1000 | 8 |
| 9 | 1001 | 9 |
| 10 | 1010 | A |
| 11 | 1011 | B |
| 12 | 1100 | C |
| 13 | 1101 | D |
| 14 | 1110 | E |
| 15 | 1111 | F |

### Base64 (trecho da tabela — múltiplos de 16)

| Decimal | Binário | Base64 |
|---|---|---|
| 0 | 000000 | A |
| 16 | 010000 | Q |
| 32 | 100000 | g |
| 48 | 110000 | w |
| 63 | 111111 | / |

## Como converter entre bases

O caminho mostrado em aula para conversão passa por:

- **Decimal → Binário**: divisões sucessivas por 2
- **Decimal → Octal**: divisões sucessivas por 8
- **Decimal → Hexadecimal**: divisões sucessivas por 16
- Também é possível converter usando **polinômios** (soma de potências da base) ou consultando uma **tabela** pronta (para conversões diretas entre binário, octal e hexadecimal).

## Exemplos práticos do uso dessas bases

- **Endereço IPv6**: é um número de 128 bits, escrito de forma compacta em **hexadecimal** (ex.: `3F80:5AD9:4176:E2FE:C512:B4B2:D6A9:5308`), pois em binário puro seria muito longo para ler.
- **Chave criptográfica (ex.: RSA 1024 bits)**: chaves criptográficas grandes costumam ser representadas em **Base64**, que empacota os bits de forma compacta usando 64 símbolos (letras maiúsculas, minúsculas, dígitos, `+` e `/`).

Esses dois exemplos mostram por que existem várias bases além do binário: hexadecimal e Base64 são formas mais compactas e legíveis de representar a mesma informação binária que o computador realmente processa.
