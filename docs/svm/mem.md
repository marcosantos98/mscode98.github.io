---
layout: docs_default
title: Manipulação de Memória
parent: SVM
nav_order: 2
---

# Manipulação de Memória
De momento a **SVM** tem dois tipos de memória.
- MemSpots: 6 células que guardam valores de 32 bits.
- MemSpace: 496 bytes que são usados para guardar _string literals_.
{: .no_toc }

## Índice
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## MemSpots

_MemSpots_ são 6 células que podem ser acedidas através das instruções `memset` e `memget` usando os números entre 0 e 5. Cada célula guarda um valor de 32 bytes ou seja pode guardar valores entre `-2147483647` e `2147483647`.

### Exemplo
```
push 10
memset 0 # coloca 10 no spot 0
push 20
memset 1 # coloca 20 no spot 1
memget 0 # coloca 10 no topo do stack
memget 1 # coloca 20 no topo do stack
plus
print
```

---

## MemSpace

_MemSpace_ é uma área com 496 bytes que armazena as _strings_ que são adicionadas no _stack_. 

### Notas
- Quando uma _string_ é adicionada, a **SVM** guarda-a na memória e colaca a localização na memória no topo do _stack_.
- Cada _string_ é separada por um _null terminator_ (0), isto é o que determina o comprimento da _string_ no momento de leitura.

### Exemplo

```
push "Hello, svm!" # Retorna o inicio da string e coloca-a na memoria.
prints
```

```
48 65 6c 6c 6f 20 57 6f 72 6c 64 21 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00

...
```

---