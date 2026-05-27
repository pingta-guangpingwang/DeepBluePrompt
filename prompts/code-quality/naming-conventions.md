---
name: TypeScript 命名与类型规范
id: prompt-code-002
type: prompt
category: 代码规范
subcategory: 命名规范
tech_stack: [TypeScript, ESLint]
style_tags: [规范编码, 可读性]
use_cases:
  - TypeScript 项目规范制定
  - 代码审查标准
score: 4.7
rating_count: 68
usage_count: 2100
last_verified: 2026-05-20
source_url:
author: prompt-store
version: 1.0
created: 2026-05-20
updated: 2026-05-20
summary: TypeScript 命名规范与类型设计指南，覆盖变量、函数、接口、枚举、泛型等命名约定
summary_en: TypeScript naming conventions and type design guide covering variables, functions, interfaces, enums, generics, and more
facets:
  role:
    - R010
    - R011
  domain:
    - D010
  task:
    - T080
  tech:
    - K011
  paradigm:
    - P064
  format:
    - F053
  level:
    - L030
---

# TypeScript 命名与类型规范

## 命名约定
- **文件**：PascalCase 组件文件，camelCase 工具/hook 文件，kebab-case 配置文件
- **接口/类型**：PascalCase，Props 以 Props 结尾，如 `UserCardProps`
- **枚举**：PascalCase，成员 PascalCase，如 `enum Status { Active, Inactive }`
- **变量/函数**：camelCase，布尔值以 is/has/can 开头
- **常量**：UPPER_SNAKE_CASE
- **泛型参数**：单字母大写，T 默认，K/V 键值，E 元素

## 类型设计
1. 优先使用 interface 定义对象类型，type 用于联合/交叉/映射类型
2. 避免 any，用 unknown 替代需要动态类型的位置
3. 使用 const as const 获取字面量类型
4. 善用 Partial/Pick/Omit/Required 工具类型派生
5. 使用 discriminated union 处理多态数据

## 禁止事项
- 禁止 `as` 强制类型断言绕过类型检查
- 禁止 `@ts-ignore`，用 `@ts-expect-error` 替代
- 禁止 `export default`，统一命名导出
