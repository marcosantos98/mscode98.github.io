---
layout: docs_default
title: Como usar a SVM
parent: SVM
nav_order: 0
---

# Como usar a SVM
A SVM é escrita em C, ou seja, para usar necessita de um compilador de C.
{: .no_toc }

## Índice
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Requerimentos

- cmake
- GNU make
- C compiler

---

## Como compilar

1. Clone o repositório
```
git clone https://github.com/mscode98/svm.git
```
2. Entre na pasta
```
cd svm
```
3. Use **cmake** para gerar o makefile 
```
cmake .
```
4. Use **make** para criar o executable
```
make
```

---

## Como usar

De momento o único argumento necessário é o ficheiro com as instruções para a SVM.

```
./svm <input>.svm
```

[Clica aqui](https://github.com/mscode98/svm/tree/master/examples) para exemplos.

---