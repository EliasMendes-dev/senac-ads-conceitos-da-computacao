# Exercícios — Sistemas Numéricos (resolvidos com a tabela HEX‑BIN‑DEC)

A ideia central é simples: cada coluna da tabela representa uma potência de 2. Quando o bit está ligado, marcamos **1** nessa coluna; depois somamos os valores das colunas marcadas para obter o número em decimal. Para hexadecimal, os bits são agrupados de **4 em 4** (peso local **8‑4‑2‑1**); para octal, de **3 em 3** (peso local **4‑2‑1**) — sempre contando da direita para a esquerda.

Nos exercícios 2, 6 e 7, alguns números passam de 512, então a tabela foi estendida com as colunas **1024** e **2048** para manter a progressão das potências de 2.

> Dica de estudo: a tabela funciona como uma "escala de pesos". O bit mais à direita vale 1, o próximo vale 2, depois 4, 8, 16, 32, 64, 128, e assim por diante.

---

## 1) Conversão Binário → Decimal

**Passo a passo — 00001100₂:**
1. Colunas de peso: 128, 64, 32, 16, 8, 4, 2, 1.
2. Bits ligados: 8 e 4.
3. Soma: 8 + 4 = 12.
4. Resultado: **12**.

| Nº binário | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | = Decimal |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|
| 00001100₂ | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | **12** |
| 00000100₂ | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | **4** |
| 00000111₂ | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | **7** |
| 00000010₂ | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | **2** |
| 11001111₂ | 1 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | **207** |
| 00100010₂ | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | **34** |
| 01000100₂ | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | **68** |
| 10000001₂ | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | **129** |
| 10000000₂ | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | **128** |

---

## 2) Binário → Decimal (par ou ímpar) — tabela estendida

| Nº binário | 1024 | 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | = Decimal | Par/Ímpar |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|:---:|
| 11100001100₂ | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | **1804** | par |
| 11000001001₂ | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 1 | **1545** | ímpar |
| 00000111111₂ | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | **63** | ímpar |
| 00000010001₂ | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | **17** | ímpar |
| 11001111000₂ | 1 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | **1656** | par |

*(O último dígito, coluna 1, decide par/ímpar: marcado = ímpar.)*

---

## 3) Conversão Decimal → Binário

**Passo a passo — 100₁₀:**
1. Maior potência de 2 que cabe em 100: 64. Resto: 36.
2. Maior potência que cabe em 36: 32. Resto: 4.
3. Maior potência que cabe em 4: 4. Resto: 0.
4. Colunas usadas: 64, 32 e 4. Resultado: **001100100₂**.

| Decimal | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | = Binário |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|
| 100₁₀ | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 0 | 0 | **001100100₂** |
| 200₁₀ | 0 | 1 | 1 | 0 | 0 | 1 | 0 | 0 | 0 | **011001000₂** |
| 101₁₀ | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 0 | 1 | **001100101₂** |
| 202₁₀ | 0 | 1 | 1 | 0 | 0 | 1 | 0 | 1 | 0 | **011001010₂** |
| 432₁₀ | 1 | 1 | 0 | 1 | 1 | 0 | 0 | 0 | 0 | **110110000₂** |
| 65₁₀ | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | **001000001₂** |
| 4₁₀ | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | **000000100₂** |
| 8₁₀ | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | **000001000₂** |
| 27₁₀ | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 1 | 1 | **000011011₂** |

---

## 4) Conversão Binário → Octal

Agrupamos os bits de **3 em 3**, da direita para a esquerda, usando o peso local **4‑2‑1** em cada grupo. Como os números têm 8 bits (não é múltiplo de 3), completamos o grupo mais à esquerda com um **zero de preenchimento**, virando 9 bits ao todo.

**Passo a passo — 00001100₂:**
1. Complete com um zero à esquerda: 0 00001100 → **000 001 100** (9 bits, já agrupados de 3 em 3).
2. Converta cada grupo com peso 4‑2‑1: `000` = 0 · `001` = 1 · `100` = 4·1+2·0+1·0 = 4.
3. Junte os dígitos na ordem: 0, 1, 4 → **14₈**.

| Nº binário | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | Agrupado de 3 (c/ zero à esquerda) | = Octal |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|
| 00001100₂ | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 000·001·100 | **14₈** |
| 00000100₂ | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 000·000·100 | **4₈** |
| 00000111₂ | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 000·000·111 | **7₈** |
| 00000010₂ | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 000·000·010 | **2₈** |
| 11001111₂ | 1 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | 011·001·111 | **317₈** |
| 00100010₂ | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 000·100·010 | **42₈** |
| 01000100₂ | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | 001·000·100 | **104₈** |
| 10000001₂ | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 010·000·001 | **201₈** |
| 10000000₂ | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 010·000·000 | **200₈** |

---

## 5) Conversão Binário → Hexadecimal

Mesmos bits do exercício 1, agrupados de 4 em 4 (peso local 8‑4‑2‑1).

**Passo a passo — 00001100₂:**
1. Agrupe de 4 em 4: **0000 1100**.
2. `0000` = 0 · `1100` = 8+4 = 12 = **C**.
3. Resultado: **0C₁₆**.

| Nº binário | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | = Hex |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|
| 00001100₂ | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | **0C₁₆** |
| 00000100₂ | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | **04₁₆** |
| 00000111₂ | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | **07₁₆** |
| 00000010₂ | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | **02₁₆** |
| 11001111₂ | 1 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | **CF₁₆** |
| 00100010₂ | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | **22₁₆** |
| 01000100₂ | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | **44₁₆** |
| 10000001₂ | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | **81₁₆** |
| 10000000₂ | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | **80₁₆** |

---

## 6) Conversão Hexadecimal → Binário  |  7) Hexadecimal → Decimal

Mesmos valores hexa nos dois exercícios, então seguem juntos (tabela estendida até 2048, pois ABC₁₆ passa de 512).

**Passo a passo — 200₁₆:**
1. O dígito **2** ocupa a casa dos 256 (segundo dígito hexa), então vale 2 × 256 = **512**.
2. Os dígitos seguintes são 0, então não somam nada.
3. Em binário, o 512 corresponde a apenas um bit ligado: **001000000000₂**.
4. Em decimal: **512**.

| Hex | 2048 | 1024 | 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | = Binário | = Decimal |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|
| 200₁₆ | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 001000000000₂ | **512** |
| 15₁₆ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 000000010101₂ | **21** |
| F₁₆ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 000000001111₂ | **15** |
| B2₁₆ | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 0 | 1 | 0 | 000010110010₂ | **178** |
| 70₁₆ | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 000001110000₂ | **112** |
| 1A0₁₆ | 0 | 0 | 0 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 000110100000₂ | **416** |
| ABC₁₆ | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 0 | 0 | 101010111100₂ | **2748** |
| 3FF₁₆ | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 001111111111₂ | **1023** |

**Como ler o hexadecimal pela tabela:** agrupe as colunas de 4 em 4 (da direita p/ esquerda) e some o peso local 8‑4‑2‑1 de cada grupo.
Exemplo com **B2₁₆**: grupo (128,64,32,16) = 1,0,1,1 → 8+2+1 = **11 = B**; grupo (8,4,2,1) = 0,0,1,0 → **2**. Resultado: **B2**.
