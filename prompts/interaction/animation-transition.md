---
name: 动画与过渡效果指南
id: prompt-int-002
type: prompt
category: 交互逻辑
subcategory: 动画过渡
tech_stack: [React, CSS, Framer Motion, Tailwind CSS]
style_tags: [流畅动画, 微交互, 性能优化]
use_cases:
  - 页面路由切换动画
  - 组件进出场效果
  - 骨架屏加载动画
  - 滚动揭示动画
score: 4.6
rating_count: 0
usage_count: 0
last_verified: 2026-05-25
source_url:
author: prompt-store
version: 1.0
created: 2026-05-25
updated: 2026-05-25
summary: 使用 CSS Transition 和 Framer Motion 设计流畅的页面过渡、组件动画和微交互效果
summary_en: Design fluid page transitions, component animations, and micro-interactions using CSS Transition and Framer Motion
---

# 动画与过渡效果指南

请根据以下规范设计动画与过渡效果：

## 设计原则

1. **动效有目的**: 每个动画传达状态变化或提供反馈, 非纯装饰
2. **自然缓动**: 微交互用 `ease-out`(进入)和 `ease-in`(离开), 推荐:
   - 标准: `cubic-bezier(0.4, 0, 0.2, 1)`, 入场: `cubic-bezier(0, 0, 0.2, 1)`
3. **时长控制**: 微交互 100-200ms, 组件进出场 200-300ms, 页面过渡 300-500ms
4. **尊重用户**: 检测 `prefers-reduced-motion`, 减少动效

## 场景实现

### 路由切换
使用 Framer Motion AnimatePresence 包裹路由出口, 页面进入:
`opacity: 0→1` + `translateY: 12px→0`, 300ms ease-out; 离开: opacity 反向 200ms

### 列表进场(stagger)
容器 `staggerChildren: 0.05`, 子项 `{ opacity: 0, y: 16 } → { opacity: 1, y: 0 }`, 200ms

### 悬停微交互
1. 卡片: scale(1.02) + shadow-lg, 点击 scale(0.98), 200ms
2. 按钮: 背景色加深 10%, 禁用状态无动效
3. 链接: 下划线从左滑入(伪元素 + transform-origin: left)

### 骨架屏
shimmer 动画: `background: linear-gradient(90deg, #e5e7eb 25%, #f3f4f6 50%, #e5e7eb 75%); background-size: 200% 100%`, 1.5s infinite ease-in-out, 暗色模式适配

### 模态框
打开: 遮罩 fade 200ms + 内容 scale(0.95→1)/opacity(0→1) 300ms, 关闭反向 200ms; 点遮罩关闭时弹窗轻微抖动: `x: [0, -4, 4, -4, 0]`

## 性能规则

1. **只动 transform 和 opacity**: 仅触发 Composite, 避免 Layout/Paint
2. **禁止动画 width/height**: 用 transform: scale 替代
3. **will-change**: 频繁动画元素设置, 动画结束移除
4. **降级**: 低端设备/不支持时回退静态状态

## 注意事项
- 移动端减少 blur 和复杂阴影; 键盘操作不触发移入动画
- 滚动揭示用 `whileInView` + `once: true` 避免重复
- Framer Motion layout prop 避免在大型列表使用
