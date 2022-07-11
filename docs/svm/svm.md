---
layout: docs_default
title: SVM
nav_order: 1
has_children: true
permalink: docs/svm
---

# SVM - Smoll Virtual Machine

SVM ou _Smool Virtual Machine_, é um programa escrito em C que é capaz de reproduzir instruções básicas de um processador.
{: .fs-6 .fw-300 }

## Exemplo:

Um programa que soma `10+10` e retorna o resultado na consola.

```
push 10
push 10
plus
print
```

[Aqui](https://github.com/mscode98/svm/tree/master/examples) tens vários exemplos, como por exemplo, calcular os primeiros 20 números da regra de ouro (_Fibonnaci Numbers_).