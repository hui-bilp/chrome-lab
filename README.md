# chrome-lab

未来感创意网页作品集 —— 10 个纯单文件 HTML 作品，无构建步骤，浏览器直接打开即可运行。

涉及 WebGPU / WebGL / Canvas / 生成艺术 / 实时粒子系统等方向，代码全部内联（HTML + CSS + JS 三合一），零依赖、离线可用。

## 作品列表

| 文件 | 标题 | 简介 |
|---|---|---|
| `1.html` | KAIRO VOSS | 创意技术者个人主页，暗色编辑风格排版 |
| `2.html` | GLOW — 发光球体 | 发光球体交互演示 |
| `3.html` | HEXFORGE // 熔核蜂巢矩阵 | 蜂巢格状熔核矩阵，FORGE CONTROL 控制台 |
| `4.html` | KILN | 创意开发者单页，极简暗色 |
| `5.html` | KAI | 创意开发者 & 界面设计师主页：界面、案例研究 |
| `6.html` | 知微 ZHWEI | 中文大模型平台概念页，静态排版 + 数据叙事 |
| `7.html` | SOLSTICE — Golden Hour Feed | 黄金时刻信息流，Aurel Sol 品牌概念 |
| `8.html` | SOLIDUS · 体积等值面工作站 | 体数据等值面（iso-surface）可视化工作站 |
| `9.html` | AURELIAN // ORBIT | GPU 实时音视觉作品 |
| `10.html` | VESPER | 创意技术者作品集，实时渲染风格 |

## 使用

无需安装依赖，双击任意 `.html` 文件即可在浏览器中打开：

```bash
# 或者用任意静态服务器（可选）
python -m http.server 8000
# 然后访问 http://localhost:8000/1.html
```

## 技术说明

- 单文件架构：每个作品独立为一个 HTML 文件，内联全部样式与脚本
- 渲染技术：Canvas 2D、WebGL、WebGPU（按作品）
- 无外部 CDN 依赖（或仅有少量字体/库引用，见各文件源码）
