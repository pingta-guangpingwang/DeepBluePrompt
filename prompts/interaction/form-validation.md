---
name: 表单校验与提交交互
id: prompt-int-001
type: prompt
category: 交互逻辑
subcategory: 表单校验
tech_stack: [React, React Hook Form, Zod, TypeScript]
style_tags: [表单交互, 用户体验, 即时反馈]
use_cases:
  - 复杂表单前端校验
  - 异步提交状态管理
  - 多步骤表单验证
  - 管理后台 CRUD 表单
score: 4.7
rating_count: 0
usage_count: 0
last_verified: 2026-05-25
source_url:
author: prompt-store
version: 1.0
created: 2026-05-25
updated: 2026-05-25
summary: 完整的表单校验、提交反馈、错误提示交互设计，包含前端校验和异步提交状态管理
summary_en: Complete form validation, submission feedback, and error handling interaction design with client-side validation and async submission state management
facets:
  occupation:
    - O251
  skill:
    - S52
    - S125
  knowledge:
    - K01
  transversal:
    - T41
  format:
    - F01
  level:
    - L02
---

# 表单校验与提交交互

请根据以下规范实现表单校验和提交交互：

## 校验策略

### 前端即时校验
1. 使用 React Hook Form 管理状态, Zod 定义 Schema, resolvers 桥接
2. 校验时机: onBlur 字段校验 + onSubmit 全量校验
3. 校验层级: 必填 → 格式(正则) → 业务规则(密码强度/一致性)
4. 异步唯一性校验(用户名等)设 500ms 防抖, 显示 "检测中..."

### 错误提示设计
1. 错误信息紧贴输入框下方, 红色(#ef4444)文字+边框, 配 error 图标
2. 内容简短具体: "密码长度 8-20 位" 而非 "密码无效"
3. 200ms ease-out 淡入动画, 使用 aria-invalid 和 aria-describedby

## 提交交互

### 状态管理
1. 按钮: idle → loading(禁用+旋转图标) → success(✓) → idle
2. 提交中所有输入框 disabled, 阻止重复提交
3. 网络异常 toast 提示, 表单保留已填数据

### 成功与失败
1. 成功: 绿色成功提示 2 秒后消失; 跳转类延迟 1.5s 展示过渡提示
2. 字段错误: 映射到对应字段下方, 全局错误: 表单顶部 banner
3. 建立服务端错误码到用户友好提示的映射表
4. 提交失败不清空数据, 长表单自动滚动到首个人错误字段

## 代码示例

```tsx
const formSchema = z.object({
  email: z.string().min(1, '请输入邮箱').email('邮箱格式不正确'),
  password: z.string().min(8, '密码至少8位').max(20, '密码最多20位'),
}).refine(data => data.password === data.confirmPassword, { message: '两次密码不一致', path: ['confirmPassword'] });

const { register, handleSubmit, formState: { errors, isSubmitting } } = useForm({
  resolver: zodResolver(formSchema), mode: 'onBlur'
});
```

## 注意事项
- 敏感字段不清空仅在用户主动刷新后生效
- 支持 Enter 提交, Tab 切换, Escape 取消
- 文件上传显示进度条; 弹窗提交成功后关闭弹窗并刷新列表
