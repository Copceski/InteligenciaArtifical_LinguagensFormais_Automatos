# 8. Exercício guiado

## Exercício 1 — Sufixo `00`

Sobre Σ={0,1}, construa uma ER para todas as palavras que terminam em `00`.

**Sua expressão:**  
`(0|1)*00`

## Exercício 2 — Exatamente dois `a`

Sobre Σ={a,b}, construa uma ER para palavras que possuem exatamente dois símbolos `a` e qualquer quantidade de `b`.

**Sua expressão:**  
`b*ab*ab*`

## Exercício 3 — Identificador acadêmico

Construa uma Regex prática para um identificador que:

- começa com duas letras maiúsculas;
- possui três algarismos em seguida;
- termina opcionalmente com uma letra minúscula;
- não admite caracteres extras.

**Sua expressão:**  
`^[A-Z]{2}[0-9]{3}[a-z]?$`

# 9. Desafio final — Código de matrícula acadêmica

## Produção do estudante

**Regex:**  
`^(CCO|ESW|SIS)-(2024|2025|2026|2027|2028|2029)-[0-9]{4}-(M|T|N)$`

**Justificativa por blocos:**  
`(CCO|ESW|SIS)` representa os cursos.  
`(2024|2025|2026|2027|2028|2029)` representa os anos permitidos.  
`[0-9]{4}` representa exatamente quatro algarismos.  
`(M|T|N)` representa os turnos.  
`^` e `$` impedem caracteres extras.

**Dois novos casos válidos:**  
1. `CCO-2028-1234-T`  
2. `SIS-2024-0005-M`

**Dois novos casos inválidos e motivo:**  
1. `CCO-2030-1234-M` — ano fora do intervalo.  
2. `ESW-2026-123-N` — número com apenas três algarismos.

## Perguntas para justificar

**1. Qual subexpressão representa a escolha entre cursos?**

`(CCO|ESW|SIS)`

**2. Como o intervalo de anos foi limitado sem aceitar `2030`?**

Colocando somente os anos permitidos, de `2024` até `2029`.

**3. Por que `{4}` é diferente de `+` no bloco numérico?**

`{4}` exige exatamente quatro algarismos. O `+` aceita um ou mais.

**4. Qual é a função das âncoras?**

`^` indica o início e `$` indica o fim da entrada.

**5. Sua expressão aceita alguma cadeia que viola as regras? Como os testes sustentam a resposta?**

Não. Os testes válidos e inválidos verificam as regras de curso, ano, número e turno.

# 11. Perguntas de reflexão

**1. Toda expressão regular formal representa uma linguagem regular?**

Sim.

**2. Toda linguagem regular pode ser representada por uma expressão regular?**

Sim.

**3. Qual é a relação entre uma ER, um NFA e um DFA?**

Os três representam linguagens regulares. Uma ER pode ser convertida em NFA e depois em DFA.

**4. Qual é a diferença entre uma expressão regular teórica e as extensões de motores de programação?**

A expressão regular teórica possui os operadores básicos. Os motores de programação possuem recursos extras.

**5. Por que um autômato finito reconhece paridade, mas não consegue contar arbitrariamente e comparar duas quantidades sem limite?**

Porque possui uma quantidade limitada de estados e não tem memória ilimitada.

**6. Por que {aⁿbⁿ | n≥0} não é regular?**

Porque seria necessário guardar a quantidade de `a` para comparar com a quantidade de `b`, e um autômato finito não consegue fazer isso.

**7. O que muda ao passarmos de linguagens regulares para linguagens livres de contexto?**

As linguagens livres de contexto podem usar uma pilha, permitindo trabalhar com problemas que precisam de mais memória.
