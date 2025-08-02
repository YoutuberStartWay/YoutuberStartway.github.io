---
title: 05.【GitHub Pages 】如何擁有免費的個人主頁
date: 2025-08-01 00:00:00 +0900
categories: [资源分享]
tags: [Prompts]
image:
  path: /assets/img/img05.png
  alt: image alternative text
---

# 🚀 使用 Jekyll 和 Chirpy 搭建 GitHub Pages 博客教程

> 适用于 macOS 和 Windows 系统用户  
> 最终效果：一个托管在 GitHub 上的个性化博客网站

---

## 目录

1. [安装 Jekyll](#install-jekyll)
2. [安装 Git](#install-git)
3. [登录 GitHub](#login-github)
4. [创建 GitHub Pages 仓库](#create-repo)
5. [使用 jekyll-theme-chirpy 主题](#use-chirpy)

---

## 1. 安装 Jekyll {#install-jekyll}

官方网站：  
👉 [https://jekyllrb.com/](https://jekyllrb.com/)

### 💻 macOS 用户

1. 安装 Homebrew（若未安装）：
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. 安装 Ruby（Jekyll 依赖）：
   ```bash
   brew install ruby
   ```

3. 配置环境变量（建议添加到 `~/.zshrc` 或 `~/.bash_profile`）：
   ```bash
   export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
   ```

   然后执行：
   ```bash
   source ~/.zshrc
   ```

4. 安装 Jekyll 和 Bundler：
   ```bash
   gem install --user-install bundler jekyll
   ```

---

### 🖥️ Windows 用户

1. 安装 Ruby（包含 DevKit）：  
   下载地址 👉 [https://rubyinstaller.org/](https://rubyinstaller.org/)

2. 安装后，在终端（CMD 或 PowerShell）执行：
   ```bash
   gem install bundler jekyll
   ```

3. 验证安装：
   ```bash
   jekyll -v
   ```

---

## 2. 安装 Git {#install-git}

官网地址：  
👉 [https://git-scm.com/](https://git-scm.com/)

### 安装步骤：

- macOS 用户可使用 Homebrew：
  ```bash
  brew install git
  ```

- Windows 用户请前往官网下载并安装。

安装完成后，可通过以下命令验证：
```bash
git --version
```

---

## 3. 登录 GitHub {#login-github}

1. 注册或登录 [GitHub 官网](https://github.com/)
2. 可选：配置 Git 本地用户名和邮箱（用于提交记录）：
   ```bash
   git config --global user.name "你的用户名"
   git config --global user.email "你的邮箱"
   ```

---

## 4. 创建 GitHub Pages 仓库 {#create-repo}

1. 前往 GitHub，点击右上角 **New repository**
2. 命名格式为：  
   ```
   your-username.github.io
   ```
3. 建议勾选初始化仓库（Add a README file）

---

## 5. 使用 jekyll-theme-chirpy 主题 {#use-chirpy}

项目地址：  
👉 [https://github.com/cotes2020/jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy)

### 快速开始

1. **Fork** 仓库：
   点击右上角 "Fork" 到自己的 GitHub 账户下。

2. **克隆仓库到本地**：
   ```bash
   git clone https://github.com/你的用户名/jekyll-theme-chirpy.git
   cd jekyll-theme-chirpy
   ```

3. **安装依赖**：
   ```bash
   bundle install
   ```

4. **本地运行项目**：
   ```bash
   bundle exec jekyll s
   ```
   打开浏览器访问：`http://localhost:4000`

5. **部署到 GitHub Pages**：
   - 推送修改到主分支，GitHub 会自动构建并部署。
   - 访问网址：`https://你的用户名.github.io/`

---

