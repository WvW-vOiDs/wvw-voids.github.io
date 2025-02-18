---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #

date: "{{ .Date }}"
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
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




<!-- ================================ 参考文献 ================================= -->
# References
