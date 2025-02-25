---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #

date: "2025-02-21T15:54:59+08:00"
title: "Should know"
# author: "Me" # ["Me", "You"]

tags: []
# categories: [] # 舍弃使用, 通过文件夹结构确定 category

# description: "Description 将会在single page顶部展示."
# summary: "Summary 将会在list page展示."
# hideSummary: false # 如果写summary就取消注释

# **************************************************************************** #
#                                     页面设置                                     #
# **************************************************************************** #
# =================================== model ================================== #
draft: true
# weight: 1 # 需要置顶时使用

# ================================= component ================================ #
# ShowToc: false # 默认true
# TocOpen: false # 默认true

# ShowReadingTime: true # 默认false
# ShowWordCount: true # 默认false

# searchHidden: true # 默认false

# =================================== cover ================================== #
# cover:
#     image: "<image path/url>" # image path/url

#     alt: "<alt text>" # alt text
#     caption: "<text>" # display caption under cover
#     relative: false # To use relative path for cover image, used in hugo Page-bundles
#     hidden: true # only hide on current single page

# **************************************************************************** #
#                                     其他设置                                     #
# **************************************************************************** #

# ================================== mathjax ================================= #
# mathjax: false # 禁止 mathjax 渲染 latex 公式
---

<!-- ================================= 正文 ================================== -->
# Fourier 级数, Fourier 积分 和 Fourier 变换

## 周期函数的 Fourier 级数

假设函数 \(f(x)\) 的周期为 \(\lambda\) (\(k \equiv 2\pi/\lambda\)), 则

\[
\begin{aligned}
    f(x)&=\frac{a_0}{2}+\sum_{n=1}^{\infty}\left( a_n \cos(nkx) + b_n \sin(nkx) \right)\\
    &= \sum_{n=-\infty}^{\infty}\left( c_n \cos(nkx) + d_n \sin(nkx) \right)\\
    &= \sum_{n=-\infty}^{\infty} g_n e^{inkx}.
\end{aligned}
\]

其中,

\[
\left\{
\begin{aligned}
    a_n&= \frac{2}{\lambda} \int_0^\lambda  f(y)\cos(nky) \, \dd y,\\
    b_n&= \frac{2}{\lambda} \int_0^\lambda  f(y)\sin(nky) \, \dd y.
\end{aligned}
\right.
\]

\[
\left\{
\begin{aligned}
    c_n&= \frac{1}{\lambda} \int_0^\lambda  f(y)\cos(nky) \, \dd y,\\
    d_n&= \frac{1}{\lambda} \int_0^\lambda  f(y)\sin(nky) \, \dd y.
\end{aligned}
\right.
\]

\[
    g_n= \frac{1}{\lambda} \int_0^\lambda  f(y)e^{-inky} \, \dd y.
\]


<!-- ================================ 参考文献 ================================= -->
# References
