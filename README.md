# DeepBluePrompt · 深蓝提示词库

深蓝工坊生态 — AI 开发提示词种子库。每个提示词为自包含 Markdown 文件，YAML 头部提供机器可解析的结构化元数据，正文可直接复制使用。**零 SDK 依赖，任何 AI 工具可用。**

## 为什么需要它

AI 开发中，高质量提示词决定了代码生成的质量上限。这个仓库收录经过实战验证的提示词模板，覆盖 UI 设计、代码质量、交互细节、风格预设四大领域，供 AI 在生成代码时作为规范和参考。

## 使用方式

### 任何 AI 工具
```bash
git clone https://github.com/pingta-guangpingwang/DeepBluePrompt.git
```
直接阅读 `prompts/` 下的 Markdown 文件，复制粘贴到你的 AI 对话中即可。

### 驾驭工程（Claude Harness Desktop）
启动时自动同步，AI 根据当前开发任务自动匹配相关提示词注入上下文。也可在资源市场面板手动浏览检索。

### AI 程序化检索
先读 `manifest.ai.json`（精简索引，Token 消耗降低 60%），命中后按需读取详情文件。`manifest.json` 为完整索引，供前端面板和 HTML 站点使用。

## 目录结构

```
DeepBluePrompt/
├── README.md
├── _TEMPLATE.md               ← 贡献模板
├── manifest.json               ← 完整索引（人类+前端用）
├── manifest.ai.json            ← AI 精简索引（低 Token）
└── prompts/
    ├── ui-design/              ← 布局排版、配色搭配、响应式适配
    ├── code-quality/           ← 规范编码、性能优化、模块化拆分
    ├── interaction/            ← 动画过渡、表单校验、异步请求
    └── style-presets/          ← 极简风、科技赛博风、商务稳重风
```

## 文件格式规范

每个 `.md` 文件由 YAML Frontmatter 头部和 Markdown 正文组成：

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
source_url: https://github.com/example/repo
author: 作者
summary: 一句话摘要
---

# 提示词标题

正文内容...
```

## 当前种子资源

| 提示词 | 分类 | 技术栈 | 评分 |
|--------|------|--------|------|
| React 编码规范 | code-quality | React, TypeScript, ESLint | 5 |
| 命名规范指南 | code-quality | TypeScript, JavaScript | 4 |
| 动画过渡设计 | interaction | React, Framer Motion, CSS | 4 |
| 表单校验设计 | interaction | React, Zod, React Hook Form | 5 |
| 商务稳重风 | style-presets | React, Ant Design, Tailwind | 4 |
| 科技赛博风 | style-presets | React, Tailwind, Three.js | 4 |
| 极简干净风 | style-presets | React, Tailwind, Shadcn UI | 4 |
| 暗色主题配色 | ui-design | CSS, Tailwind, Design Tokens | 5 |
| 响应式布局 | ui-design | CSS Grid, Flexbox, Container Queries | 5 |

## 贡献指南

1. **Fork** 本仓库
2. 参考 `_TEMPLATE.md` 格式创建或修改提示词文件
3. 确保 YAML Frontmatter 必填字段完整（`id` `name` `type` `category` `score` `summary`）
4. **提交 PR** → CI 自动检查格式和死链 → 合并后 DeepBlueBuilder 自动更新索引和 HTML 站点

## 评分机制

| 维度 | 权重 | 说明 |
|------|------|------|
| 可复用性 | 40% | 是否可以直接复制使用 |
| 覆盖度 | 30% | 覆盖场景的广度 |
| 质量 | 30% | 提示词的精细度和效果 |

## License

MIT
