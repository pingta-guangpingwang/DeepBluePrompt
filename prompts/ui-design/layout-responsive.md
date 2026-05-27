---
name: 响应式布局设计提示词
id: prompt-ui-001
type: prompt
category: UI设计
subcategory: 布局排版
tech_stack: [React, CSS, Tailwind CSS, Flexbox, Grid]
style_tags: [响应式, 现代简约, 移动优先]
use_cases:
  - 电商页面自适应布局
  - 后台管理系统多端适配
  - 官网首页响应式排版
score: 4.8
rating_count: 86
usage_count: 2300
last_verified: 2026-05-20
source_url:
author: prompt-store
version: 1.0
created: 2026-05-20
updated: 2026-05-20
summary: 采用移动优先策略设计响应式布局，使用CSS Grid做主框架、Flexbox处理组件内排列，搭配Tailwind断点实现多端自适应
summary_en: Mobile-first responsive layout using CSS Grid for the main framework and Flexbox for component alignment, with Tailwind breakpoints for multi-device adaptation
facets:
  occupation:
    - O251
    - O216
  skill:
    - S54
    - S91
  knowledge:
    - K01
    - K10
  transversal:
    - T12
  format:
    - F01
  level:
    - L03
---

# 响应式布局设计

请按照以下要求设计页面响应式布局：

## 设计原则
1. **移动优先**：先设计移动端（375px），再通过断点向上扩展到平板（768px）和桌面（1280px）
2. **Grid 主框架 + Flexbox 组件内排列**：页面整体使用 CSS Grid 划分区域，组件内部用 Flexbox 对齐
3. **断点策略**：sm: 640px / md: 768px / lg: 1024px / xl: 1280px / 2xl: 1536px
4. **流体排版**：使用 clamp() 函数实现字体和间距的流体缩放
5. **图片适配**：使用 srcset + sizes 属性，不同断点加载不同分辨率图片

## 布局要求
- 移动端：单列布局，导航折叠为汉堡菜单
- 平板：双列布局，侧边栏可折叠
- 桌面：三列或侧边栏 + 主内容区 + 辅助面板

## 注意事项
- 避免固定宽度，使用百分比或 fr 单位
- 触摸目标最小 44x44px
- 内容区域最大宽度 1200px，居中显示
- 测试横屏和竖屏两种方向
