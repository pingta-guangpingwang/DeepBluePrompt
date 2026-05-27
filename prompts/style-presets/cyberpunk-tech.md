---
name: 科技赛博朋克风格
id: prompt-style-002
type: prompt
category: 风格定制
subcategory: 科技风
tech_stack: [React, CSS, Three.js, Tailwind CSS]
style_tags: [赛博朋克, 科技感, 霓虹灯, 未来感]
use_cases:
  - 区块链/Web3 项目官网
  - 数据可视化大屏
  - 游戏主题页面
  - AI/科技产品落地页
score: 4.5
rating_count: 0
usage_count: 0
last_verified: 2026-05-25
source_url:
author: prompt-store
version: 1.0
created: 2026-05-25
updated: 2026-05-25
summary: 赛博朋克科技风格设计模板，霓虹灯效果、深色背景、发光边框、科技感配色
summary_en: Cyberpunk sci-fi style design template with neon glow effects, dark backgrounds, luminous borders, and futuristic color schemes
facets:
  role:
    - R010
    - R040
  domain:
    - D080
  task:
    - T053
  tech:
    - K030
  paradigm:
    - P043
  format:
    - F010
  level:
    - L030
---

# 科技赛博朋克风格

请使用以下赛博朋克科技风格规范实现界面：

## 设计语言

赛博朋克美学 = 高科技 + 低生活, 视觉核心: 黑暗都市 + 霓虹灯光 + 数字网格

## 配色方案

### 背景层级
- 页面底色: #0a0a0f → 卡片: #161b22 → 输入框: #0d1117

### 霓虹色系统
- 主强调: #00ff88(青绿) — 主按钮、关键图标
- 辅强调: #ff0055(品红) — 警告、高亮标签
- 信息色: #00d4ff(电光蓝) — 链接、提示
- 次要: #ffaa00(琥珀) — 评级/评分

### 文字
- 主文字: #e0e0e0, 次要: #8892a4, 禁用: #586069
- 标题可用霓虹色, 正文严格浅灰确保可读性

### 发光效果
```css
.neon-cyan { text-shadow: 0 0 7px #00ff88, 0 0 10px #00ff88, 0 0 21px #00ff88; }
.neon-border { border: 1px solid #00ff88; box-shadow: 0 0 5px #00ff8840, inset 0 0 5px #00ff8820; }
```

## 视觉元素

### 背景
1. 纯黑底色叠加 CSS 网格线(透明度 5-8%, 40px 间距): linear-gradient 绘制十字网格
2. 可选: Canvas/Three.js 粒子动画, 微光点漂浮

### 边框与字体
- 卡片: 1px 发光边框, 可切角 `clip-path: polygon(...)` 增强科技感
- 标题字体: Orbitron/Rajdhani, 全大写 + 字间距 0.2em
- 正文字体: JetBrains Mono/Source Code Pro(等宽)

## 组件风格

### 按钮
默认透明背景+霓虹边框+霓虹文字, 300ms 过渡; 悬停霓虹填充+发光增强 50%; 禁用灰色无发光

### 卡片/面板
背景 #161b22 半透明 0.85, 边框 `1px solid rgba(0,255,136,0.15)`, 悬停发光增强+scale(1.02), 圆角 4px

### 数据展示
数字跳动动画; 进度条霓虹渐变+发光边缘; 图表暗色主题, 线条霓虹色, 网格线极淡

## 注意事项
- 发光节制: 仅关键元素, 避免视觉过载; 正文严格不用霓虹色
- 移动端降低发光强度, 减少粒子; 尊重 prefers-reduced-motion
- 提供亮色模式切换入口(可选)
