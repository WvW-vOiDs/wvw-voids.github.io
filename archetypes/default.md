---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #

date: "{{ .Date }}"
title: "{{ replace .File.ContentBaseName "-" " " | title }}"

tags: []
categories: []

# **************************************************************************** #
#                                     页面设置                                     #
# **************************************************************************** #
# =================================== model ================================== #
draft: true

# ================================= component ================================ #
ShowToc: true
# TocOpen: true

# ShowReadingTime: true
# ShowBreadCrumbs: false

# =================================== cover ================================== #
# cover:
#     image: "<image path/url>"
#     # can also paste direct link from external site
#     # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false # To use relative path for cover image, used in hugo Page-bundles

#     responsiveImages: false # 减少网站的生成时间和大小可以禁用

# ================================== mathjax ================================= #
# mathjax: false # 禁止 mathjax 渲染 latex 公式
---