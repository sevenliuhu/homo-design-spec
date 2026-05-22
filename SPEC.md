# DESIGN.md 规范 v1.0 — 技术规格

## YAML Frontmatter 完整字段

```yaml
---
brand:
  name: string                    # 品牌名称
  tagline: string                 # 品牌标语
  
colors:
  primary: hex                    # 主色
  primary_hover: hex              # 主色悬停
  secondary: hex                  # 辅色
  accent: hex                     # 强调色
  success: hex                    # 成功色
  warning: hex                    # 警告色
  error: hex                      # 错误色
  background:
    light: hex
    dark: hex
  text:
    primary: hex
    secondary: hex
    inverse: hex

typography:
  sans: font-family               # 无衬线字体
  serif: font-family              # 衬线字体（可选）
  mono: font-family               # 等宽字体（可选）
  scale: [size...]                # 字号阶梯（px）
  weights:                        # 字重映射
    regular: 400
    medium: 500
    semibold: 600
    bold: 700

spacing:
  unit: px                        # 基础单位
  scale: [size...]                # 间距阶梯

border:
  radius:
    sm: px
    md: px
    lg: px
    full: px

shadow:
  sm: "x y blur color"
  md: "x y blur color"
  lg: "x y blur color"

motion:
  duration:
    fast: ms
    normal: ms
    slow: ms
  easing:
    default: cubic-bezier(...)

breakpoints:
  sm: px
  md: px
  lg: px
  xl: px
---
```
