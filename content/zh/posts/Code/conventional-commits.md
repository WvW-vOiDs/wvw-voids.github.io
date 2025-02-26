---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #

date: "2025-02-26T13:12:51+08:00"
title: "Conventional Commits"
# author: "Me" # ["Me", "You"]

tags: ["git", "blog"]
# categories: [] # 舍弃使用, 通过文件夹结构确定 category

# description: "Description 将会在single page顶部展示."
# summary: "Summary 将会在list page展示."
# hideSummary: false # 如果写summary就取消注释

# **************************************************************************** #
#                                     页面设置                                     #
# **************************************************************************** #
# =================================== model ================================== #
draft: false
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
mathjax: false # 禁止 mathjax 渲染 latex 公式
---

<!-- ================================= 导言 ================================== -->

> 本文由 **deepseek-r1** 辅助生成.

<!-- ================================= 正文 ================================== -->

[**Conventional Commits**](https://www.conventionalcommits.org/) 是一种广泛使用的提交消息规范, 旨在通过标准化的格式提高提交信息的可读性、可维护性, 并支持自动化工具 (如生成 CHANGELOG、语义化版本控制等).

---

## Conventional Commits 核心格式

提交消息的格式为:

```
<type>[optional scope]: <subject>
[optional body]
[optional footer]
```

### 1. 类型 (Type)
| 类型          | 说明                                                                 |
|---------------|--------------------------------------------------------------------|
| `feat`        | **新增功能** (对应语义化版本的 `minor`)                               |
| `fix`         | **修复 Bug** (对应语义化版本的 `patch`)                              |
| `docs`        | **文档更新** (如 README、注释等)                                     |
| `style`       | **代码样式调整** (不影响逻辑的格式修改, 如空格、缩进等)                 |
| `refactor`    | **代码重构** (既不修复 Bug 也不新增功能的结构性修改)                   |
| `perf`        | **性能优化**                                                       |
| `test`        | **测试代码更新** (单元测试、集成测试等)                               |
| `build`       | **构建工具或依赖更新** (如 Webpack、npm 等)                          |
| `ci`          | **CI 配置修改** (如 GitHub Actions、Travis 等)                      |
| `chore`       | **其他杂项修改** (不涉及代码或文档的改动, 如清理临时文件)               |
| `revert`      | **回滚之前的提交**                                                  |

### 2. 作用域 (Scope, 可选)
- 描述修改的影响范围 (如模块、组件、文件等), 用括号包裹:

```
feat(login): add OAuth2 support
fix(api): handle null response
```

### 3. 主题 (Subject)
- 简短描述 (不超过 50 字符), 使用**祈使语气** (如 "add" 而非 "added"):

```
docs: update installation guide
```

### 4. 正文 (Body, 可选)
- 详细说明修改内容和动机, 与主题用空行隔开:

```
fix: prevent memory leak in data processing

- Add cleanup logic for event listeners
- Update error handling in async functions
```

### 5. 脚注 (Footer, 可选)
- **关联 Issue**: 关闭的问题或任务 (如 `Closes #123`)
- **破坏性变更**: 用 `BREAKING CHANGE:` 标记重大变更 (触发语义化版本的 `major` 版本) :

```
feat: remove deprecated API

BREAKING CHANGE: The `oldMethod()` is no longer supported.
```

---

## 完整示例

```
feat(auth): add password reset endpoint

- Add POST /auth/reset-password endpoint
- Send email notification on reset request

Closes #45
BREAKING CHANGE: Remove deprecated `resetByUsername` method
```

---

## 扩展规范 (Angular 风格)
许多团队基于 [Angular Commit Guidelines](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format) 扩展, 例如:
- `ci`: 持续集成配置
- `build`: 构建系统
- `perf`: 性能优化
- `revert`: 回滚提交

## 自定义规范 (服务于博客)

在个人博客场景中, 大部分提交可能确实围绕**内容创作**和**文档维护**展开. 如果觉得 `docs` 类型过于笼统, 可以基于 Conventional Commits 的灵活性和你的实际需求, **自定义更细分的类型**. 以下是一些针对博客优化的类型建议:

---

### 自定义类型建议
| 类型            | 适用场景                                                                 |
|-----------------|-------------------------------------------------------------------------|
| `post`          | **发布新文章** (替代 `feat`, 专用于内容创作)                              |
| `update`        | **更新已有文章** (如补充段落、修正过时信息)                                |
| `meta`          | **元数据修改** (如调整文章分类、标签、SEO关键词等)                         |
| `seo`           | **SEO 优化** (如添加 Alt 文本、优化标题、调整 sitemap)                    |
| `media`         | **媒体文件更新** (新增/替换图片、视频、音频等)                             |
| `fix`           | **修正错误** (如文章中的技术错误、死链修复等)                              |
| `style`         | **排版或样式调整** (如 Markdown 格式、代码高亮、CSS 美化)                 |
| `translate`     | **翻译内容** (新增或更新多语言版本)                                       |
| `refactor`      | **内容重构** (重新组织文章结构, 优化逻辑流)                               |
| `chore`         | **维护性任务** (如更新依赖、清理冗余文件)                                 |

---

### 使用示例
#### 1. 发布新文章

```
post: add article about quantum computing basics
```
或带作用域 (如分类):
```
post(physics): introduce quantum entanglement
```

#### 2. 更新现有文章

```
update: add code example to CSS animation guide
```

#### 3. 调整标签/分类

```
meta: add 'AI' tag to GPT-4 article
```

#### 4. SEO 优化

```
seo: optimize meta description for homepage
```

#### 5. 媒体文件管理

```
media: replace header image with WebP format
```

---

### 扩展建议
1. **保持类型简洁**:

   避免过度细分 (如 `image`/`video` 可统一为 `media`), 否则会增加维护成本.

2. **结合作用域 (Scope)**:

   用作用域标记文章分类、技术栈等, 增强可读性:
   ```
   update(react): migrate class component to hooks
   fix(linux): correct permission command in tutorial
   ```

3. **在 README 中记录规范**:

   在博客仓库的文档中明确自定义类型, 便于协作 (示例) :
   ```markdown
   ## 提交规范
   - `post`: 新文章
   - `update`: 更新旧文
   - `meta`: 标签/分类调整
   - `seo`: 搜索引擎优化
   ...
   ```

---

### 与标准 Conventional Commits 的对比
| 标准类型       | 博客场景替代类型       | 优势                                                                 |
|----------------|-----------------------|----------------------------------------------------------------------|
| `docs`         | `post`, `update`      | 明确区分新内容创作与旧内容更新                                       |
| `feat`         | `post`                | 避免将文章发布与技术功能新增混用                                     |
| `style`        | `style`               | 保留, 用于代码或排版美化                                             |
| `chore`        | `chore`               | 保留, 用于维护任务                                                   |

---

### 何时仍应使用 `docs`？

如果博客包含**非文章类文档** (如项目说明、API 文档) , 可保留 `docs` 类型:
```
docs: update contribution guidelines
```


<!-- ================================ 参考文献 ================================= -->
# References

- https://www.mikeperham.com/2025/01/30/conventional-commits/
- https://www.conventionalcommits.org/
- https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format