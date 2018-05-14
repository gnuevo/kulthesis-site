---
title: "Baseline Experiments"
date: 2018-05-12T12:38:21+09:00
draft: true
---

### Chapter 6

Audios from experiments in chapter 6.


## Average of the output

{{< titles "original" "averaged" "non-averaged" >}}
{{< audio original averaged non_averaged >}}


## relu vs tanh activations

{{< titles "original" "relu" "tanh" >}}
{{< audio original relu tanh >}}


## Different input and code sizes

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< audio tanh_1024_100 >}} | {{< audio tanh_1024_200 >}} | {{< audio tanh_1024_400 >}} |
| 2048 | {{< audio tanh_2048_100 >}} | {{< audio tanh_2048_200 >}} | {{< audio tanh_2048_400 >}} |
| 4096 | {{< audio tanh_4096_100 >}} | {{< audio tanh_4096_200 >}} | {{< audio tanh_4096_400 >}} |


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
| 1024_200 | {{< audio tanh_1024_200 >}} | {{< audio tanh_weight01_1024_200 >}} | {{< audio tanh_weight03_1024_200 >}} |
| 2048_200 | {{< audio tanh_2048_200 >}} | {{< audio tanh_weight01_2048_200 >}} | {{< audio tanh_weight03_2048_200 >}} |
| 4096_200 | {{< audio tanh_4096_200 >}} | {{< audio tanh_weight01_4096_200 >}} | {{< audio tanh_weight03_4096_200 >}} |


## Quantisation

We use linear quantisation and mu-law.

| size | original | linear quantisation | mu-law quantisation |
|----|----------|---------------------|---------------------|
| 1024_200 | {{< audio tanh_1024_200 >}} | {{< audio tanh_linear_1024_200 >}} | {{< audio tanh_mu_1024_200 >}} |
| 2048_200 | {{< audio tanh_2048_200 >}} | {{< audio tanh_linear_2048_200 >}} | {{< audio tanh_mu_2048_200 >}} |
| 4096_200 | {{< audio tanh_4096_200 >}} | {{< audio tanh_linear_4096_200 >}} | {{< audio tanh_mu_4096_200 >}} |


## Other instruments
