---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #

date: "2025-02-26T13:12:51+08:00"
title: "Conventional Commits"
# author: "Me" # ["Me", "You"]

tags: ["git"]
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

> 以下文本由 **deepseek-r1** 辅助生成, 原始 Prompt 为：
> "git 中有哪些常用的 Conventional Commits 有没有一个比较完善的标准？"

<!-- ================================= 正文 ================================== -->

[**Conventional Commits**](https://www.conventionalcommits.org/) 是一种广泛使用的提交消息规范, 旨在通过标准化的格式提高提交信息的可读性、可维护性, 并支持自动化工具 (如生成 CHANGELOG、语义化版本控制等).

---

## **Conventional Commits 核心格式**

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
  ```bash
  feat(login): add OAuth2 support
  fix(api): handle null response
  ```

### 3. 主题 (Subject)
- 简短描述 (不超过 50 字符), 使用**祈使语气** (如 "add" 而非 "added"):
  ```bash
  docs: update installation guide
  ```

### 4. 正文 (Body, 可选)
- 详细说明修改内容和动机, 与主题用空行隔开:
  ```bash
  fix: prevent memory leak in data processing

  - Add cleanup logic for event listeners
  - Update error handling in async functions
  ```

### 5. 脚注 (Footer 可选) 
- **关联 Issue**: 关闭的问题或任务 (如 `Closes #123`)
- **破坏性变更**: 用 `BREAKING CHANGE:` 标记重大变更 (触发语义化版本的 `major` 版本) :
  ```bash
  feat: remove deprecated API

  BREAKING CHANGE: The `oldMethod()` is no longer supported.
  ```

---

## **完整示例**
```bash
feat(auth): add password reset endpoint

- Add POST /auth/reset-password endpoint
- Send email notification on reset request

Closes #45
BREAKING CHANGE: Remove deprecated `resetByUsername` method
```

---

## **扩展规范 (Angular 风格) **
许多团队基于 [Angular Commit Guidelines](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format) 扩展, 例如:
- `ci`: 持续集成配置
- `build`: 构建系统
- `perf`: 性能优化
- `revert`: 回滚提交



<!-- ================================ 参考文献 ================================= -->
# References

- https://www.mikeperham.com/2025/01/30/conventional-commits/
- https://www.conventionalcommits.org/
- https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format