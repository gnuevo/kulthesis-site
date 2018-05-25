---
title: "Loss function and custom loss function"
date: 2018-05-13T18:03:46+09:00
draft: false
---

## Audios

This is a dump of all the audios generated

**For the relu activation function**

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< audio "chapter6_500/relu_1024_100" >}} | {{< audio "chapter6_500/relu_1024_200" >}} | {{< audio "chapter6_500/relu_1024_400" >}} |
| 2048 | {{< audio "chapter6_500/relu_2048_100" >}} | {{< audio "chapter6_500/relu_2048_200" >}} | {{< audio "chapter6_500/relu_2048_400" >}} |
| 4096 | {{< audio "chapter6_500/relu_4096_100" >}} | {{< audio "chapter6_500/relu_4096_200" >}} | {{< audio "chapter6_500/relu_4096_400" >}} |


**For the tanh activation funciton**

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< audio "chapter6_500/tanh_1024_100" >}} | {{< audio "chapter6_500/tanh_1024_200" >}} | {{< audio "chapter6_500/tanh_1024_400" >}} |
| 2048 | {{< audio "chapter6_500/tanh_2048_100" >}} | {{< audio "chapter6_500/tanh_2048_200" >}} | {{< audio "chapter6_500/tanh_2048_400" >}} |
| 4096 | {{< audio "chapter6_500/tanh_4096_100" >}} | {{< audio "chapter6_500/tanh_4096_200" >}} | {{< audio "chapter6_500/tanh_4096_400" >}} |


## Vanishing of the output

As explained in the document, output for _relu_ vanishes for big input sizes.
This doesn't have for _tanh_ activations.
However, the numerical error measure is sometimes smaller for _relu_ rather than for _tanh_.

**Results for `input_size=4096`**

| activation | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| _relu_ activation | {{< audio "chapter6_500/relu_4096_100" >}} | {{< audio "chapter6_500/relu_4096_200" >}} | {{< audio "chapter6_500/relu_4096_400" >}} |
| _tanh_ activation | {{< audio "chapter6_500/tanh_4096_100" >}} | {{< audio "chapter6_500/tanh_4096_200" >}} | {{< audio "chapter6_500/tanh_4096_400" >}} |
