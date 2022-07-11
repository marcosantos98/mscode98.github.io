---
layout: docs_default
title: Set de instruções
parent: SVM
nav_order: 1
---

# Set de instruções
Atualmente, a SVM contém 23 instruções, tendo entre elas instruções de _debug_, operações matemáticas, manipulação do _stack_ e manipulação de memória.
{: .no_toc }

## Índice
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Manipulação do stack
- `push` coloca um número ou copia uma _string literal_ para a memória.
- `dup` copia o valor que está no topo do _stack_ e coloca-o no topo do _stack_.
- `halt` pára o execução do programa.
- `drop` remove o valor que esta no topo do _stack_.
- `jmp` move o _instruction pointer_ para o valor atríbuido.
- `jneq` move o _instruction pointer_ para o valor atríbuido se o valor no topo do _stack_ não for 1.
- `print` escreve o valor no topo do _stack_ na consola.
- `prints` escreve a _string literal_ na consola.
- `memset` guarda o valor no topo do _stack_ no spot atríbuido.
- `memget` retorna o valor guardado no spot atríbuido.

---

## Instruções de teste
- `dump` escreve na consola os valores no _stack_.
- `dropall` remove todos os valores no _stack_.

---

## Condições e operações matemáticas

- `plus, minus, mult, div, mod` consume os dois últimos valores no _stack_ e coloca o resultado no topo do _stack_.
- `equal, nequal` consume os dois últimos valores no _stack_ e compare se são iguais. Retorna 1 ou 0, e o valor é colocado no topo do _stack_.
- `lt` consume os dois últimos valores no _stack_ e compare se é menor. Retorna 1 ou 0, e o valor é colocado no topo do _stack_.
- `lteq` consume os dois últimos valores no _stack_ e compare se é menor ou igual. Retorna 1 ou 0, e o valor é colocado no topo do _stack_..
- `gt` consume os dois últimos valores no _stack_ e compare se é maior.Retorna 1 ou 0, e o valor é colocado no topo do _stack_.
- `gteq` consume os dois últimos valores no _stack_ e compare se é maior ou igual. Retorna 1 ou 0, e o valor é colocado no topo do _stack_.

---