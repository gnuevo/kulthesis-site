---
title: "Loss function and custom loss function"
date: 2018-05-13T18:03:46+09:00
draft: false
---

## Audios

This is a dump of all the audios generated

**For the relu activation funciton**

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< audio baseline500_relu_1024_100 >}} | {{< audio baseline500_relu_1024_200 >}} | {{< audio baseline500_relu_1024_400 >}} |
| 2048 | {{< audio baseline500_relu_2048_100 >}} | {{< audio baseline500_relu_2048_200 >}} | {{< audio baseline500_relu_2048_400 >}} |
| 4096 | {{< audio baseline500_relu_4096_100 >}} | {{< audio baseline500_relu_4096_200 >}} | {{< audio baseline500_relu_4096_400 >}} |


**For the tanh activation funciton**

| input_size | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| 1024 | {{< audio baseline500_tanh_1024_100 >}} | {{< audio baseline500_tanh_1024_200 >}} | {{< audio baseline500_tanh_1024_400 >}} |
| 2048 | {{< audio baseline500_tanh_2048_100 >}} | {{< audio baseline500_tanh_2048_200 >}} | {{< audio baseline500_tanh_2048_400 >}} |
| 4096 | {{< audio baseline500_tanh_4096_100 >}} | {{< audio baseline500_tanh_4096_200 >}} | {{< audio baseline500_tanh_4096_400 >}} |


## Vanishing of the output

As explained in the document, output for _relu_ vanishes for big input sizes.
This doesn't have for _tanh_ activations.
However, the numerical error measure is sometimes smaller for _relu_ rather than for _tanh_.

**Results for `input_size=4096`**

| activation | code_size=100 | code_size=200 | code_size=400 |
|----|----------|---------------------|---------------------|
| _relu_ activation | {{< audio baseline500_relu_4096_100 >}} | {{< audio baseline500_relu_4096_200 >}} | {{< audio baseline500_relu_4096_400 >}} |
| _tanh_ activation | {{< audio baseline500_tanh_4096_100 >}} | {{< audio baseline500_tanh_4096_200 >}} | {{< audio baseline500_tanh_4096_400 >}} |
