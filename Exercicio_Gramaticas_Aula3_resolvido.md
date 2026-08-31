# Exercícios Práticos para Fixação

![Exercícios Práticos para Fixação](Exercicio_Gramaticas_Aula3.png)

## Bloco 1 — Derivação

Dada:

$$
G_1: S \rightarrow aS \mid b
$$

### A) Gere a palavra `aaab`.

**Resposta:**

$$
S \Rightarrow aS \Rightarrow aaS \Rightarrow aaaS \Rightarrow aaab
$$

### B) Explique como você sabe que a derivação terminou.

**Resposta:** A derivação terminou porque não há mais nenhum não terminal. A palavra final é formada somente por símbolos terminais.

---

## Bloco 2 — GLC

Dada:

$$
G_2: S \rightarrow aSb \mid \varepsilon
$$

### A) Gere uma palavra `aaabbb`.

**Resposta:**

$$
S \Rightarrow aSb \Rightarrow aaSbb \Rightarrow aaaSbbb \Rightarrow aaabbb
$$

### B) É possível gerar `aabbb`? Justifique.

**Resposta:** Não. A gramática sempre produz a mesma quantidade de `a` e `b`. `aabbb` possui 2 `a` e 3 `b`.

---

## Bloco 3 — Classificação

Classifique como Regular ou Livre de Contexto:

$$
S \rightarrow aA \mid A \rightarrow b
$$

**Resposta:** **Regular.**

A gramática é linear à direita, pois o não terminal aparece no final da produção.
