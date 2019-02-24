---
layout: wiki
title: Fourier Transform
categories: Math
description: 傅里叶变换。
keywords: FT
---

## 公式

**FT**

正变换：

$$
F(\omega) = \int^{\infty}_{-\infty} f(t)e^{-iwt}dt
$$

逆变换：

$$
f(t) = \frac{1}{2\pi}\int^{\infty}_{-\infty} F(\omega)e^{iwt}d\omega
$$

**DTFT**

正变换：

$$
X(\omega) = \sum^{\infty}_{n=-\infty} x_ne^{-iwn}
$$

逆变换：

$$
x_n = \frac{1}{2\pi}\int^{\infty}_{-\infty} X(\omega)e^{iwn}d\omega
$$

**DFT**

正变换：

$$
X[k] = \sum^{N-1}_{n=0} x_ne^{-i\frac{2\pi}{N}kn}
$$

逆变换：

$$
x_n = \frac{1}{N}\sum^{N-1}_{k=0} X[k]e^{i\frac{2\pi}{N}kn}
$$

**Parseval 定理**

$$
\sum^{N-1}_{n=0}\vert x[n]\vert ^2 = \frac{1}{N} \sum^{N-1}_{k=0}\vert X[k]\vert ^2
$$

**性质**

1. 时域(频域)卷积定理：一个域卷积等于另一个域相乘
2. Parseval 定理：信号经过傅里叶变换能量守恒
3. 一个域的连续性对应另一个域的周期性（由1推导）

**FT、DTFT、DFT的关系**

FT将信号连续信号变换为时域中的连续频谱，因为计算机只能模拟离散信号，所以将连续信号采样，即与单位脉冲序列相乘，则在频域上会与单位脉冲信号卷积，变为连续周期频谱（单位脉冲序列的傅里叶变换还是单位脉冲序列），即DTFT。但是计算机仍然不能模拟频域上的连续频谱，于是在频域上对连续频谱采样得到离散频谱，即与单位脉冲序列相乘，则在时域上与单位脉冲序列卷积，变为周期离散信号，时域和频域上都截取一个周期，即DFT。

## 常见变换对
<center><img src="/images/wiki/Fourier_pairs.png"></center>
<center><img src="/images/wiki/coherent_incoherent.png"></center>
<center><img src="/images/wiki/FT_table.png"></center>
