---
title: "Baseline"
date: 2018-05-13T18:02:32+09:00
draft: false
---

### Chapter 6

Audios from experiments in chapter 6.


## Average of the output

{{< titles "original" "averaged" "non-averaged" >}}
{{< soundcloud "original" "averaged" "non_averaged" >}}


## relu vs tanh activations

Comparison of _relu_ and _tanh_ for `input_size=1024; hidden_size=100`.

{{< titles "original" "relu" "tanh" >}}
{{< soundcloud original "relu_1024_100" "tanh_1024_100" >}}


## Different input and code sizes

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< soundcloud "tanh_1024_100" >}} | {{< soundcloud "tanh_1024_200" >}} | {{< soundcloud "tanh_1024_400" >}} |
| 2048 | {{< soundcloud "tanh_2048_100" >}} | {{< soundcloud "tanh_2048_200" >}} | {{< soundcloud "tanh_2048_400" >}} |
| 4096 | {{< soundcloud "tanh_4096_100" >}} | {{< soundcloud "tanh_4096_200" >}} | {{< soundcloud "tanh_4096_400" >}} |

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
| 1024_200 | {{< soundcloud "tanh_1024_200" >}} | {{< soundcloud "tanh_weight01_1024_200" >}} | {{< soundcloud "tanh_weight03_1024_200" >}} |
| 2048_200 | {{< soundcloud "tanh_2048_200" >}} | {{< soundcloud "tanh_weight01_2048_200" >}} | {{< soundcloud "tanh_weight03_2048_200" >}} |
| 4096_200 | {{< soundcloud "tanh_4096_200" >}} | {{< soundcloud "tanh_weight01_4096_200" >}} | {{< soundcloud "tanh_weight03_4096_200" >}} |


## Quantisation

We use linear quantisation and mu-law.

| size | original | linear quantisation | mu-law quantisation |
|----|----------|---------------------|---------------------|
| 1024_200 | {{< soundcloud "tanh_1024_200" >}} | {{< soundcloud "tanh_linear_1024_200" >}} | {{< soundcloud "tanh_mu_1024_200" >}} |
| 2048_200 | {{< soundcloud "tanh_2048_200" >}} | {{< soundcloud "tanh_linear_2048_200" >}} | {{< soundcloud "tanh_mu_2048_200" >}} |
| 4096_200 | {{< soundcloud "tanh_4096_200" >}} | {{< soundcloud "tanh_linear_4096_200" >}} | {{< soundcloud "tanh_mu_4096_200" >}} |


## Vanishing of the output

As explained in the document, output for _relu_ vanishes for big input sizes.
This doesn't have for _tanh_ activations.
However, the numerical error measure is sometimes smaller for _relu_ rather than for _tanh_.


### Relu totally distorts the output

| code_size=200 | input_size=1024 | input_size=2048 | input_size=4096 |
|----|----------|---------------------|---------------------|
| _relu_ activation | {{< soundcloud "baseline500_relu_1024_200" >}} | {{< soundcloud "baseline500_relu_2048_200" >}} | {{< soundcloud "baseline500_relu_4096_200" >}} |

### Vanishing of the output

**Results for `input_size=4096`**
For this size of the input, _relu_ completely destroys the signal and outputs just silence.

| activation | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| _relu_ activation | {{< soundcloud "baseline500_relu_4096_100" >}} | {{< soundcloud "baseline500_relu_4096_200" >}} | {{< soundcloud "baseline500_relu_4096_400" >}} |
| _tanh_ activation | {{< soundcloud "baseline500_tanh_4096_100" >}} | {{< soundcloud "baseline500_tanh_4096_200" >}} | {{< soundcloud "baseline500_tanh_4096_400" >}} |

## Other instruments
