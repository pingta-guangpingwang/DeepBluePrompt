---
name: 暗色主题配色方案
id: prompt-ui-002
type: prompt
category: UI设计
subcategory: 配色搭配
tech_stack: [CSS, Tailwind CSS, CSS Variables]
style_tags: [暗色主题, 科技感, 护眼模式]
use_cases:
  - 代码编辑器配色
  - 数据大屏暗色模式
  - 开发者工具界面
score: 4.6
rating_count: 52
usage_count: 1800
last_verified: 2026-05-20
source_url:
author: prompt-store
version: 1.0
created: 2026-05-20
updated: 2026-05-20
summary: 设计专业的暗色主题配色体系，使用CSS变量管理色彩层级，确保WCAG AA级对比度标准，支持亮/暗双模式切换
summary_en: Professional dark theme color system using CSS variables for color hierarchy management, ensuring WCAG AA contrast standards with light/dark mode switching
facets:
  role:
    - R010
    - R040
  domain:
    - D010
  task:
    - T053
  tech:
    - K030
  paradigm:
    - P043
  format:
    - F010
  level:
    - L020
---

# 暗色主题配色方案

## 色彩体系
使用 CSS 变量管理，确保亮色/暗色模式一键切换：

### 背景层级
- 基础背景：#0f172a (slate-900) — 页面底色
- 卡片背景：#1e293b (slate-800) — 组件容器
- 悬浮态背景：#334155 (slate-700) — hover 状态
- 输入框背景：#0f172a — 表单元素

### 文字层级
- 主要文字：#f1f5f9 (slate-100)
- 次要文字：#94a3b8 (slate-400)
- 辅助文字：#64748b (slate-500)
- 禁用文字：#475569 (slate-600)

### 强调色
- 主色：#6366f1 (indigo-500)
- 成功：#22c55e (green-500)
- 警告：#f59e0b (amber-500)
- 错误：#ef4444 (red-500)

## 对比度要求
- 正文文字 ≥ 4.5:1 (WCAG AA)
- 大号文字 ≥ 3:1
- 交互组件边框 ≥ 3:1

## 实现方式
使用 Tailwind dark: 前缀或 CSS 变量切换：
```css
:root { --bg-base: #ffffff; --text-primary: #1f2937; }
.dark { --bg-base: #0f172a; --text-primary: #f1f5f9; }
```
