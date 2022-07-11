---
layout: docs_default
title: Futuros melhoramenos
parent: SVM
nav_order: 3
---

# O que pode ser melhorado
- Melhorar as instruções **jmp** e **jneq**, pois de momento o utilizador tem que utilizar números para alterar o _instruction pointer_. Isto pode ser melhorado usando _labels_.

```
label [a]
push 1
push 2
lt
jneq b
plus
dup
dup
jmp a
label [b]
```
- Melhorar a propagação de erros.
- Operações para manipulação de bits.
- Versão WebAssembly. Este ponto já esta parcialmente integrado, mas não tem suporte para abrir ficheiros.
- Extensão para o VSCode.
