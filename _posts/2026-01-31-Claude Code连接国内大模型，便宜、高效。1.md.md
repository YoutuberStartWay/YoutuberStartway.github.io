---
title: Claude Code连接国内大模型，便宜、高效。
date: 2026-01-31 00:00:00 +0900
categories: [资源分享]
tags: [文档]
image:
  path: /assets/img/截屏2026-01-31 16.31.06.png.png
  alt: image alternative text
---

**开发工具接入官方文档地址：**

[https://docs.bigmodel.cn/cn/coding-plan/tool/claude](https://docs.bigmodel.cn/cn/coding-plan/tool/claude)

### 一、编辑或新增 `settings.json` 文件

```jsx
# 编辑或新增 `settings.json` 文件
# MacOS & Linux 为 `~/.claude/settings.json`
# Windows 为`用户目录/.claude/settings.json`
# 新增或修改里面的 env 字段
# 注意替换里面的 `your_zhipu_api_key` 为您上一步获取到的 API Key
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "your_zhipu_api_key",
    "ANTHROPIC_BASE_URL": "https://open.bigmodel.cn/api/anthropic",
    "API_TIMEOUT_MS": "3000000",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1,
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "glm-4.5-air",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "glm-4.7",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "glm-4.7"
  }
}
```

### 二、再编辑或新增 `.claude.json` 文件

```jsx
# 再编辑或新增 `.claude.json` 文件
# MacOS & Linux 为 `~/.claude.json`
# Windows 为`用户目录/.claude.json`
# 新增 `hasCompletedOnboarding` 参数
{
  "hasCompletedOnboarding": true
}
```

### 三、进入ClaudeCode确认

首先确认系统默认的模型名称

![這是圖片](assets/img/截屏2026-01-3116.31.06.png "圖片1")

| **特性** | **Haiku (轻量级)** | **Sonnet (平衡级)** | **Opus (巅峰级)** |
| --- | --- | --- | --- |
| **核心定位** | 追求极速、低成本 | 综合能力最强（目前主流） | 深度推理、复杂逻辑 |
| **智力表现** | 基础逻辑，适合简单任务 | 极强，尤其是 **3.5 Sonnet** | 极高，擅长多步骤复杂推理 |
| **响应速度** | **极快**（几乎秒回） | 快（3.5版本速度大幅提升） | 较慢（思考时间更长） |
| **价格成本** | 最便宜（甚至可以忽略不计） | 中等（性价比之王） | 最贵（通常是 Sonnet 的 5-10 倍） |
| **适合场景** | 客服机器人、文本分类、简单数据提取 | **代码编写**、文案创作、复杂分析 | 科学研究、超长文档深度解读 |
| --- | --- | --- | --- |
| **你映射后的实际模型** | **`glm-4.5-air`** | **`glm-4.7`** | **`glm-4.7`** |
| **映射后的体验** | 响应轻快，适合日常对话 | 智谱目前的最强水平 | 与 Sonnet 体验完全一致 |

然后输入/status命令查看baseUrl和模型名称，

![這是圖片](assets/img/截屏2026-01-31-16.31.59.jpg "圖片1")

可以通过/model切换模型

**`/model`**：会弹出一个交互式菜单，让你用上下键选择（Haiku / Sonnet / Opus）。

完成了！