

## 1. Operadores Lógicos

| Operador | Significado |
| -------- | ----------- |
| `∧`      | E           |
| `∨`      | OU          |
| `¬`      | NÃO         |

* **E (`∧`)** → as duas condições devem ser verdadeiras.
* **OU (`∨`)** → pelo menos uma deve ser verdadeira.
* **NÃO (`¬`)** → inverte o valor lógico.

---

## 2. Palavra Vazia — ε

A **palavra vazia** é uma cadeia que não possui nenhum símbolo.

```text
ε
```

Seu comprimento é:

```text
|ε| = 0
```

---

## 3. Prefixos e Sufixos

Para a palavra:

```text
abc
```

### Prefixos

São as partes que aparecem **no início**:

```text
ε, a, ab, abc
```

### Sufixos

São as partes que aparecem **no final**:

```text
ε, c, bc, abc
```

---

## 4. Alfabeto — Σ

Um **alfabeto** é um conjunto finito de símbolos.

Exemplo:

```text
Σ = {a, b}
```

Nesse caso, o alfabeto possui dois símbolos: `a` e `b`.

---

## 5. Σ* — Todas as Cadeias Possíveis

`Σ*` representa **todas as cadeias possíveis** que podem ser formadas usando os símbolos de `Σ`, incluindo `ε`.

Para:

```text
Σ = {a, b}
```

Temos:

```text
Σ* = {ε, a, b, aa, ab, ba, bb, aaa, ...}
```

---

## 6. Linguagem Formal — L

Uma **linguagem formal** é um conjunto de cadeias pertencentes a `Σ*`.

Exemplo:

```text
L = {a, aa, aaa}
```

---

## 7. Gramática Formal

Uma **gramática formal** é um conjunto de regras usado para gerar palavras de uma linguagem.

É representada por:

```text
G = (V, Σ, P, S)
```

Onde:

* `V` = variáveis
* `Σ` = símbolos terminais
* `P` = regras de produção
* `S` = símbolo inicial

---

## 8. Regras de Produção

As **regras de produção** determinam como os símbolos podem ser substituídos.

Exemplo:

```text
S → aS
S → b
```

Ou, de forma abreviada:

```text
S → aS | b
```

---

## 9. Como Ler →

O símbolo:

```text
→
```

pode ser lido como:

> **"gera"**, **"produz"** ou **"pode ser substituído por"**.

Exemplo:

```text
S → aS
```

Lê-se:

> **S produz aS.**

---

## 10. Derivação de Palavras

**Derivação** é o processo de aplicar as regras da gramática para formar uma palavra.

Exemplo:

```text
S ⇒ aS
  ⇒ aaS
  ⇒ aab
```

Resultado:

```text
aab
```

---

## 11. Linguagem Gerada

A **linguagem gerada** é o conjunto de todas as palavras que podem ser produzidas pela gramática.

Para:

```text
S → aS | b
```

Podemos gerar:

```text
b
ab
aab
aaab
aaaab
...
```

Logo:

```text
L = {b, ab, aab, aaab, ...}
```

---

## 12. Atividades Práticas

### Exemplos de atividades:

* Identificar um alfabeto.
* Criar cadeias.
* Encontrar prefixos e sufixos.
* Identificar a palavra vazia.
* Construir uma linguagem.
* Criar regras de produção.
* Fazer derivações.

---

## 13. Resumo para Prova

| Conceito  | Significado                |
| --------- | -------------------------- |
| `Σ`       | Alfabeto                   |
| `ε`       | Palavra vazia              |
| `Σ*`      | Todas as cadeias possíveis |
| `L`       | Linguagem                  |
| `G`       | Gramática                  |
| `→`       | Produção/substituição      |
| `S`       | Símbolo inicial            |
| `P`       | Regras de produção         |
| Derivação | Processo de gerar palavras |

### ⭐ Para decorar

```text
Σ  → alfabeto
ε  → palavra vazia
Σ* → todas as cadeias
L  → linguagem
G  → gramática
→  → produz
S  → início
```

---

## 14. Mapa Mental

```text
📚 LINGUAGENS FORMAIS
│
├── 🔤 Alfabeto (Σ)
│   └── Conjunto de símbolos
│
├── 📝 Cadeias
│   ├── Prefixos
│   └── Sufixos
│
├── ε
│   └── Palavra vazia
│
├── ⭐ Σ*
│   └── Todas as cadeias possíveis
│
├── 📖 Linguagem (L)
│   └── Conjunto de cadeias
│
└── ⚙️ Gramática (G)
    ├── Variáveis (V)
    ├── Terminais (Σ)
    ├── Produções (P)
    └── Símbolo inicial (S)
        │
        └── Derivação
            └── Gera palavras

> **Derivação** é o processo de aplicar essas regras.

