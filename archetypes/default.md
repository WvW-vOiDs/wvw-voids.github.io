---
date: "{{ .Date }}"
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
draft: true

# params:
#     mathjax: false
---
