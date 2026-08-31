# Exercícios — Linguagens Formais e Autômatos

## 1. Alfabeto

Considere:

```text
Σ = {a, b, c}
```

### Respostas

1. **Quantidade de símbolos:** 3
2. **Símbolos:** `a`, `b`, `c`
3. **a pertence ao alfabeto?** Sim.
4. **d pertence ao alfabeto?** Não.
5. **Exemplo de palavra:** `abc`

---

## 2. Palavras sobre um alfabeto

Considere:

```text
Σ = {0, 1}
```

| Sequência | Válida? | Justificativa           |
| --------- | ------- | ----------------------- |
| `0101`    | Sim     | Possui apenas `0` e `1` |
| `00110`   | Sim     | Possui apenas `0` e `1` |
| `012`     | Não     | `2` não pertence a `Σ`  |
| `111`     | Sim     | Possui apenas `0` e `1` |
| `10a`     | Não     | `a` não pertence a `Σ`  |

---

## 3. Pertinência de símbolos e palavras

Considere:

```text
Σ = {0, 1}
```

1. `0 ∈ Σ` — **Verdadeiro**
2. `1 ∈ Σ` — **Verdadeiro**
3. `01 ∈ Σ` — **Falso**, pois `01` é uma palavra, não um símbolo.
4. `01 ∈ Σ*` — **Verdadeiro**
5. `2 ∈ Σ` — **Falso**
6. `101 ∈ Σ*` — **Verdadeiro**

---

## 4. Linguagem

Considere:

```text
L = {0, 01, 011, 0111}
```

| Palavra | Pertence a L? |
| ------- | ------------- |
| `0`     | Sim           |
| `01`    | Sim           |
| `0111`  | Sim           |
| `10`    | Não           |
| `111`   | Não           |
| `011`   | Sim           |

---

## 5. Descrevendo uma linguagem por padrão

Considere:

```text
L = {bⁿ | n ≥ 1}
```

### Cinco primeiras palavras

```text
b
bb
bbb
bbbb
bbbbb
```

### Significado de `bⁿ`

Representa `n` ocorrências do símbolo `b`.

### `bbbbbb` pertence à linguagem?

**Sim.**

```text
bbbbbb = b⁶
```

### A palavra vazia `ε` pertence?

**Não**, pois a condição é `n ≥ 1`.

---

## 6. Linguagem vazia e palavra vazia

### A) `L = ∅`

Não possui nenhuma palavra.

### B) `L = {ε}`

Possui exatamente uma palavra: `ε`.

### Respostas

* Possui uma palavra: **`L = {ε}`**
* Não possui nenhuma palavra: **`L = ∅`**
* Comprimento de `ε`: **0**

```text
∅ ≠ {ε}
```

---

## 7. Estrutura de uma gramática

Considere:

```text
G = ({S, A}, {0, 1}, P, S)
```

com:

```text
P = {S → 0A, A → 1}
```

### Respostas

* **Variáveis:** `{S, A}`
* **Terminais:** `{0, 1}`
* **Produções:** `{S → 0A, A → 1}`
* **Símbolo inicial:** `S`

### Palavra gerada

```text
S ⇒ 0A ⇒ 01
```

Resposta:

```text
01
```

---

## 8. Aplicando uma produção

Considere:

```text
S → 0S
```

### Uma vez

```text
S ⇒ 0S
```

### Duas vezes

```text
S ⇒ 0S ⇒ 00S
```

### Três vezes

```text
S ⇒ 0S ⇒ 00S ⇒ 000S
```

A derivação ainda não terminou porque o símbolo `S` continua presente.

---

## 9. Derivação completa

Considere:

```text
S → aS
S → b
```

Para gerar `aaab`:

```text
S ⇒ aS
  ⇒ aaS
  ⇒ aaaS
  ⇒ aaab
```

Portanto, `aaab` pode ser gerada pela gramática.

---

## 10. Palavras geradas por uma gramática

Considere:

```text
S → 0S
S → 1
```

### 1. `1`

Sim.

```text
S ⇒ 1
```

### 2. `01`

Sim.

```text
S ⇒ 0S ⇒ 01
```

### 3. `001`

Sim.

```text
S ⇒ 0S ⇒ 00S ⇒ 001
```

### 4. `0001`

Sim.

```text
S ⇒ 0S ⇒ 00S ⇒ 000S ⇒ 0001
```

### 5. `101`

Não.

A produção `S → 1` encerra a derivação.

### 6. `1001`

Não.

A gramática gera apenas palavras no formato:

```text
000...001
```

Ou seja, zero ou mais `0`, seguidos de um único `1`.

---

# Desafio Final

Considere:

```text
S → aS
S → b
```

## 1. A palavra `b` pode ser gerada?

**Sim.**

```text
S ⇒ b
```

## 2. A palavra `ab` pode ser gerada?

**Sim.**

```text
S ⇒ aS ⇒ ab
```

## 3. A palavra `aab` pode ser gerada?

**Sim.**

```text
S ⇒ aS ⇒ aaS ⇒ aab
```

## 4. A palavra `aaab` pode ser gerada?

**Sim.**

```text
S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab
```

## 5. A palavra `aba` pode ser gerada?

**Não.**

Depois que `S → b` é aplicado, a derivação termina. Portanto, não é possível adicionar `a` depois do `b`.

## 6. Derivação de `aaaab`

```text
S ⇒ aS
  ⇒ aaS
  ⇒ aaaS
  ⇒ aaaaS
  ⇒ aaaab
```

## 7. Padrão das palavras geradas

A gramática gera palavras formadas por **zero ou mais `a` seguidos de um único `b`**.

Exemplos:

```text
b
ab
aab
aaab
aaaab
```

Podemos representar por:

```text
L = {aⁿb | n ≥ 0}
```

---

# Resumo dos principais conceitos

| Conceito           | Significado                                          |
| ------------------ | ---------------------------------------------------- |
| `Σ`                | Alfabeto                                             |
| `a`, `b`, `0`, `1` | Símbolos                                             |
| `w`                | Palavra                                              |
| `L`                | Linguagem                                            |
| `Σ*`               | Todas as palavras possíveis sobre `Σ`, incluindo `ε` |
| `ε`                | Palavra vazia                                        |
| `∅`                | Conjunto vazio                                       |
| `w ∈ L`            | `w` pertence à linguagem                             |
| `w ∉ L`            | `w` não pertence à linguagem                         |
| `G`                | Gramática                                            |
| `V`                | Variáveis ou não terminais                           |
| `T`                | Terminais                                            |
| `P`                | Produções                                            |
| `S`                | Símbolo inicial                                      |
| `→`                | Regra de produção                                    |
| `⇒`                | Derivação                                            |
