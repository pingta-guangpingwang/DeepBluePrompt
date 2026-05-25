---
name: 商务稳重风格模板
id: prompt-style-003
type: prompt
category: 风格定制
subcategory: 商务风
tech_stack: [React, Ant Design, Tailwind CSS, TypeScript]
style_tags: [商务稳重, 企业级, 专业, 可信赖]
use_cases:
  - 企业管理后台
  - B2B SaaS 平台
  - 金融/银行系统界面
  - 政府/机构信息平台
score: 4.7
rating_count: 0
usage_count: 0
last_verified: 2026-05-25
source_url:
author: prompt-store
version: 1.0
created: 2026-05-25
updated: 2026-05-25
summary: 企业级商务风格设计模板，稳重配色、清晰信息层级、专业排版
summary_en: Enterprise-grade business style design template with restrained colors, clear information hierarchy, and professional typography
---

# 商务稳重风格模板

请使用以下商务稳重风格规范实现界面：

## 设计原则

1. **可信赖感**: 配色沉稳克制, 布局规整, 专业可靠的第一印象
2. **信息密度合理**: 用间距和层级降低认知负荷
3. **一致性优先**: 所有页面、组件、交互模式保持一致

## 配色方案

### 主色调
- 主色: #1e40af(blue-800) — 辅色: #2563eb(blue-600), 背景: #f8fafc(slate-50), 卡片: #ffffff
- 侧边栏: #1e293b(slate-800, 深色) 凸显专业感

### 文字与功能色
- 主: #0f172a / 次要: #475569 / 辅助: #94a3b8
- 功能: 成功 #059669 / 警告 #d97706 / 错误 #dc2626 / 信息 #0284c7

## 排版体系

- 字体: 中文 PingFang SC, 英文/数字 Inter(Roboto), 数字 Tabular Nums
- H1 28px/bold → H2 22px/semibold → H3 18px/medium
- 正文 14px/行高 1.6, 辅助 12px/行高 1.5(商务场景偏小字号容纳更多信息)
- 禁止装饰性字体, 全站统一

## 布局规范

### 管理后台布局
侧边栏(220px, 深色) + 头部(56px, 深蓝白字) + 主内容区(padding: 24px)

### 间距系统
- 页面内边距: 24px(桌面)/16px(移动), 卡片: 20px/间距 16px
- 表格行高: 48px/40px(紧凑), 表单项间距: 20px

## 组件风格

### 按钮
主按钮: 深蓝实心白字, 悬停加深 10%, 圆角 6px, 高 36px
次按钮: 白底+1px 边框+深蓝文字; 危险按钮红色, 操作前二次确认

### 表格
表头灰底 #f1f5f9, 12px 全大写 medium; 斑马纹+悬停行 #eff6ff; 固定表头+独立滚动, 空状态居中+操作引导

### 表单
标签左对齐, 输入框高 36px, 边框 #cbd5e1, 聚焦变主色; 必填红色星号, 分组用分割线+标题

## 数据可视化
图表主色系渐变(深蓝→浅蓝), 统计卡片大数字+趋势箭头(绿涨红跌), 仪表盘 4/3 列网格
表格支持排序筛选分页(默认 20 条/页), 右上角 CSV/Excel 导出

## 注意事项
- 批量操作: 选中浮现操作栏, 无权限功能直接隐藏(非置灰)
- 响应式: 移动端侧边栏折叠, 表格变卡片列表
