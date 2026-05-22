# DESIGN.md — 视觉身份描述规范 (HOMO 中文版)

> 基于 Google Labs visual identity description format 设计理念（14k⭐同类项目）
> 让 AI Agent 理解和应用品牌视觉系统的标准化接口

## 什么是 DESIGN.md？

DESIGN.md 是一个标准化的设计系统描述文件，采用 **YAML + Markdown 双层结构**：

- **YAML 前端**：机器可读的设计令牌（颜色、排版、圆角、间距等精确值）
- **Markdown 正文**：人类可读的设计原理（为什么及如何应用）

## 文件结构

```
DESIGN.md
├── YAML Frontmatter（设计令牌）
│   ├── colors         # 颜色系统（主色/辅色/强调色/背景/文字）
│   ├── typography     # 排版系统（字体/字号/行高/字重）
│   ├── spacing        # 间距系统（基础单位/缩放比例）
│   ├── border         # 边框/圆角
│   ├── shadow         # 阴影层级
│   ├── motion         # 动效（时长/缓动函数）
│   └── breakpoints    # 响应式断点
│
└── Markdown Body（设计原理）
    ├── 品牌定位 & 调性
    ├── 色彩原理 & 使用场景
    ├── 排版规则 & 层级
    ├── 组件设计指南
    └── WCAG 无障碍说明
```

## 示例

```yaml
---
brand:
  name: "HOMO"
  tagline: "智能体操作系统"
  
colors:
  primary: "#2563EB"
  primary_hover: "#1D4ED8"
  secondary: "#8B5CF6"
  
typography:
  sans: "'Inter', system-ui, sans-serif"
  scale: [12, 14, 16, 18, 20, 24, 30, 36, 48]

spacing:
  unit: 4
  scale: [0, 4, 8, 12, 16, 20, 24, 32, 40, 48, 64]

border:
  radius:
    sm: 4
    md: 8
    lg: 12
---
```

## 工具链

- **lint**: 自动验证 WCAG 对比度
- **diff**: 检测令牌级回归
- **render**: 从 DESIGN.md 生成完整设计系统预览页

## 为什么需要 DESIGN.md？

AI Agent 在生成视觉内容时，如果没有明确的品牌规范，输出往往不一致。
DESIGN.md 为 Agent 提供了明确的、结构化的品牌指南，确保每次输出都符合品牌调性。

## 📧 联系我们

商业合作：16208204@qq.com
