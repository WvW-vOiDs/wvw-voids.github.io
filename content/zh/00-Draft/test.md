---
date: "2024-12-30T12:03:13+08:00"
title: "Test Demo"

draft: false
ShowToc: true
TocOpen: true

tags: []
categories: []
---

本文用于测试网站功能.

## 数学公式测试

### 行内公式
*code*:
```LaTeX
这是一个行内公式 \(a^*=x-b^*\).
```

*output*:
这是一个行内公式 \(a^*=x-b^*\).


### 行间公式

这些是行间公式:

1.
*code*:
```latex
\[a^*=x-b^*.\]
```

*output*:

\[a^*=x-b^*.\]

2.
*code*:
```latex
\[ a^*=x-b^*. \]
```

*output*:

\[ a^*=x-b^*. \]

3.
*code*:
```LaTeX
\[
    a^*=x-b^*.
\]
```

*output*:

\[
    a^*=x-b^*.
\]


### physics 宏包

现在用的 Mathjax 的cdn不是很稳定, 有时候本地渲染不出来.

1.
*code*:
```latex
\[
    \mqty(1 & 2 \\ 3 & 4)
\]
```

*output*:

\[
    \mqty(1 & 2 \\ 3 & 4)
\]

2.
*code*:
```latex
\[
    \ip{\psi}{\phi}
\]
```

*output*:

\[
    \ip{\psi}{\phi}
\]


### 超过3个大括号的公式

*code*:
```LaTeX
\[
    \boldsymbol{x_{i+1}}+\boldsymbol{x_{i+2}}=\boldsymbol{x_{i+3}}
\]
```

*output*:

\[
    \boldsymbol{x_{i+1}}+\boldsymbol{x_{i+2}}=\boldsymbol{x_{i+3}}
\]


## 代码测试

### 行内代码

*code*:
```md
`This is Inline Code.`
```

*output*:
`This is Inline Code.`


### 预格式化文本 (preformatted text)

*code*:
```html
<pre>
这是一些
    预格式化的文本.
    空格 和 换行符
        都会被保留.111
</pre>
```

*output*:
<pre>
这是一些
    预格式化的文本.
    空格 和 换行符
        都会被保留.111
</pre>


### 行间代码

1. 普通\`\`\`代码块.

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
    <meta
      name="description"
      content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

2. \`\`\`代码块加语言类型声明.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
    <meta
      name="description"
      content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

3. \`\`\`代码块加语言类型声明, 并且增加行号. [^行号]

```html {linenos=true}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
    <meta
      name="description"
      content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

4. \`\`\`代码块加语言类型声明, 有行号, 并且有 <mark>高亮</mark> 代码.

```html {linenos=true,hl_lines=["2-4",8,11]}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
    <meta
      name="description"
      content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

5. 还可以设置初始行号, 和代码行号 url 的前缀. (如果需要可以把前缀设置成这段 code 的文件名等)

```html {linenos=true,hl_lines=["2-4",8,11],linenostart=199,lineanchors=prefixOfCode}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
    <meta
      name="description"
      content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```


### Github Gist

{{< gist adityatelange 376cd56ee2c94aaa2e8b93200f2ba8b5 >}}

---
## References

- [PaperMod example site.](https://github.com/adityatelange/hugo-PaperMod/blob/exampleSite/content/posts/code_syntax.md)


[^行号]: 和上一个一样是因为我默认设置了代码块有行号.