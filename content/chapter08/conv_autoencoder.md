---
title: "Convolutional autoencoder"
date: 2018-06-08T07:00:33+09:00
draft: false
---


# Experiments with the convolutional autoencoder

## Baseline

`input_size=1024, K=4`

{{< titles piano2piano piano2violin violin2piano violin2violin >}}
{{< soundcloud 1024_k4_5conv_vanilla_00 1024_k4_5conv_vanilla_01 1024_k4_5conv_vanilla_10 1024_k4_5conv_vanilla_11 >}}

## Baseline with dense core

{{< titles piano2piano piano2violin violin2piano violin2violin >}}
{{< soundcloud 1024_k4_5conv_dense64_00 1024_k4_5conv_dense64_01 1024_k4_5conv_dense64_10 1024_k4_5conv_dense64_11 >}}

## Baseline with variational core

{{< titles piano2piano piano2violin violin2piano violin2violin >}}
{{< soundcloud 1024_k4_conv5_vae64_00 1024_k4_conv5_vae64_01 1024_k4_conv5_vae64_10 1024_k4_conv5_vae64_11 >}}
