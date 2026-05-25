---
name: React 编码最佳实践
id: prompt-code-001
type: prompt
category: 代码规范
subcategory: React规范
tech_stack: [React, TypeScript, ESLint]
style_tags: [规范编码, 可维护]
use_cases:
  - React 项目初始化
  - 代码审查标准
  - 团队编码规范制定
score: 4.9
rating_count: 104
usage_count: 3200
last_verified: 2026-05-20
source_url:
author: prompt-store
version: 1.0
created: 2026-05-20
updated: 2026-05-20
summary: React + TypeScript 编码规范，覆盖组件设计、Hooks使用、状态管理、性能优化等核心实践
summary_en: React + TypeScript coding standards covering component design, Hooks usage, state management, and performance optimization best practices
---

# React 编码最佳实践

## 组件设计
1. 每个组件只做一件事，超过 200 行拆分子组件
2. Props 使用 TypeScript interface 定义，必选/可选明确区分
3. 使用 React.memo 包裹纯展示组件
4. 避免在渲染中创建内联函数和对象

## Hooks 使用
1. useEffect 必须有正确的依赖数组，禁止空依赖抑制警告
2. 自定义 Hook 以 use 开头，返回元组 [value, setter] 格式
3. 使用 useCallback 包裹传递给子组件的回调
4. 使用 useMemo 缓存昂贵计算

## 状态管理
1. UI 状态用 useState，跨组件状态用 Context
2. 服务端数据用 React Query 管理缓存
3. 复杂全局状态考虑 Zustand，避免 Redux 过度工程
4. 表单状态用 React Hook Form

## 性能优化
1. 列表渲染使用 key（唯一稳定ID，禁止用 index）
2. 大列表使用虚拟滚动（react-window）
3. 图片懒加载 + WebP 格式
4. 路由级代码分割：React.lazy + Suspense
