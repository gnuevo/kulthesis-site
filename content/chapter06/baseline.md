---
title: "Baseline"
date: 2018-05-13T18:02:32+09:00
draft: false
---

### Chapter 6

Audios from experiments in chapter 6.


## Average of the output

{{< titles "original" "averaged" "non-averaged" >}}
{{< audio original "chapter6/averaged" "chapter6/non_averaged" >}}


## relu vs tanh activations

{{< titles "original" "relu" "tanh" >}}
{{< audio original "chapter6/relu" "chapter6/tanh" >}}


## Different input and code sizes

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< audio "chapter6/tanh_1024_100" >}} | {{< audio "chapter6/tanh_1024_200" >}} | {{< audio "chapter6/tanh_1024_400" >}} |
| 2048 | {{< audio "chapter6/tanh_2048_100" >}} | {{< audio "chapter6/tanh_2048_200" >}} | {{< audio "chapter6/tanh_2048_400" >}} |
| 4096 | {{< audio "chapter6/tanh_4096_100" >}} | {{< audio "chapter6/tanh_4096_200" >}} | {{< audio "chapter6/tanh_4096_400" >}} |

## Spurious frequencies

## Custom loss function

We apply the loss function over the arquitectures with

```
input_size = [1024, 2048, 4096]
code_size = 200
activation = "tanh"
```

Results are shown below for the parameter of the loss equal to: `param=0`, equivalent
to standard loss function; `param=0.1`; and `param=0.3`.

| size | param=0.0 | param=0.1 | param=0.3 |
|----|----------|---------------------|---------------------|
| 1024_200 | {{< audio "chapter6/tanh_1024_200" >}} | {{< audio "chapter6/tanh_weight01_1024_200" >}} | {{< audio "chapter6/tanh_weight03_1024_200" >}} |
| 2048_200 | {{< audio "chapter6/tanh_2048_200" >}} | {{< audio "chapter6/tanh_weight01_2048_200" >}} | {{< audio "chapter6/tanh_weight03_2048_200" >}} |
| 4096_200 | {{< audio "chapter6/tanh_4096_200" >}} | {{< audio "chapter6/tanh_weight01_4096_200" >}} | {{< audio "chapter6/tanh_weight03_4096_200" >}} |


## Quantisation

We use linear quantisation and mu-law.

| size | original | linear quantisation | mu-law quantisation |
|----|----------|---------------------|---------------------|
| 1024_200 | {{< audio "chapter6/tanh_1024_200" >}} | {{< audio "chapter6/tanh_linear_1024_200" >}} | {{< audio "chapter6/tanh_mu_1024_200" >}} |
| 2048_200 | {{< audio "chapter6/tanh_2048_200" >}} | {{< audio "chapter6/tanh_linear_2048_200" >}} | {{< audio "chapter6/tanh_mu_2048_200" >}} |
| 4096_200 | {{< audio "chapter6/tanh_4096_200" >}} | {{< audio "chapter6/tanh_linear_4096_200" >}} | {{< audio "chapter6/tanh_mu_4096_200" >}} |


## Other instruments
