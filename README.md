# Prompt Store

优秀 AI 开发提示词汇编。每个提示词文件为自包含 Markdown，YAML 头部提供机器可解析的元数据，正文为可直接复制使用的提示词。

## 使用方式

### 任何 AI 工具
直接 clone 仓库，阅读 `prompts/` 下的 Markdown 文件。每个文件的 YAML Frontmatter 描述场景和适用技术栈，正文即提示词。

### 驾驭工程 (Claude Harness Desktop)
启动时自动同步，AI 根据开发任务自动匹配相关提示词注入上下文。也可在资源市场面板手动浏览。

### AI 检索入口
先读 `manifest.ai.json`（精简索引），命中后按需读详情文件。`manifest.json` 为完整索引，供前端面板和 HTML 生成使用。

## 目录结构

```
prompts/
├── ui-design/        # 布局排版、配色搭配、响应式适配
├── code-quality/     # 规范编码、性能优化、模块化拆分
├── interaction/      # 动画过渡、表单校验、异步请求
└── style-presets/    # 极简风、科技赛博风、商务稳重风
```

## 贡献指南

1. Fork 本仓库
2. 参考 `_TEMPLATE.md` 格式创建或修改提示词文件
3. 确保 YAML Frontmatter 完整填写
4. 提交 PR，CI 会自动检查格式

## 文件格式规范

```yaml
---
name: 提示词名称
id: prompt-xxx-001
type: prompt
category: 分类
tech_stack: [React, TypeScript]
style_tags: [极简风]
use_cases: [场景描述]
score: 4.5
source_url:
author: 作者
summary: 一句话摘要
---

# 提示词标题

正文内容...
```

## License

MIT
