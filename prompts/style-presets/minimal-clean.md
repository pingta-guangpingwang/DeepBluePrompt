---
name: 极简风格设计模板
id: prompt-style-001
type: prompt
category: 风格定制
subcategory: 极简风
tech_stack: [React, Tailwind CSS, TypeScript]
style_tags: [极简风, 留白, 干净整洁, 少即是多]
use_cases:
  - 个人博客/作品集
  - SaaS 落地页
  - 阅读类应用
  - 文档站点
score: 4.8
rating_count: 0
usage_count: 0
last_verified: 2026-05-25
source_url:
author: prompt-store
version: 1.0
created: 2026-05-25
updated: 2026-05-25
summary: 极简主义设计风格的完整提示词模板，强调留白、克制配色、清晰层级
summary_en: Minimalist design style prompt template emphasizing white space, restrained color palettes, and clear visual hierarchy
facets:
  occupation:
    - O216
    - O243
    - O251
  skill:
    - S91
  knowledge:
    - K10
  transversal:
    - T14
  format:
    - F01
  level:
    - L02
---

# 极简风格设计模板

请使用以下极简主义设计规范实现界面：

## 设计哲学

1. **少即是多**: 每个元素必须有存在理由, 移除一切非必要装饰
2. **内容优先**: 设计服务于内容, 不让视觉元素喧宾夺主
3. **留白是元素**: 负空间和内容同等重要, 页面有呼吸感

## 配色方案

- 背景: #ffffff(纯白) 或 #fafafa(微灰底色)
- 文字主色: #1a1a1a(近黑, 不用纯黑), 辅色: #6b7280(gray-500)
- 强调色: 单一色, 仅链接和关键按钮, 推荐 #2563eb(蓝) 或 #000
- 边框: #e5e7eb(gray-200), 1px solid
- 规则: 95% 黑白灰 + 5% 强调色, 不超三种灰色, 无渐变

## 排版体系

- 中文: Noto Sans SC / PingFang SC, 英文/数字: Inter / SF Pro
- 头条 32px/bold, 标题 24/20/18px 逐级, 正文 16px/行高 1.75, 辅文 14px/行高 1.5
- 正文最大宽度 680px(阅读舒适度), 通过字号/字重/颜色区分层级
- 区块间距: 80px(桌面)/48px(移动), 段落间距: 24px

## 布局规则

1. 单列中心, 页面最大宽 1200px, 内容宽 680px
2. 8px 网格系统: 所有间距为 8/16/24/32/48/64/80
3. 卡片: 白底+1px 边框, 圆角 8px, 无阴影或仅 shadow-sm
4. 导航: 固定顶部 64px, Logo 左 + 3-4 链接右, 滚动加底部 1px 分隔线

## 交互要求

1. 链接悬停: 变强调色+下划线, 150ms 过渡
2. 按钮: 文字按钮为主(outline), 强调操作用实心
3. 滚动: smooth scroll-behavior, 图片懒加载

## 禁止事项
- 禁止阴影超过 shadow-sm; 圆角超过 12px
- 禁止超 2 种字体; 禁止装饰性图标和插画
- 禁止背景图案和纹理; 禁止渐变
