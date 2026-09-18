# chrome-lab

未来感创意网页作品集 —— 10 个纯单文件 HTML 作品，无构建步骤，浏览器直接打开即可运行。

涉及 WebGPU / WebGL / Canvas / 生成艺术 / 实时粒子系统等方向，代码全部内联（HTML + CSS + JS 三合一），零依赖、离线可用。

## 作品列表

文件名按「序号 - 品牌 - 实际画面效果」命名。

| 文件 | 标题 | 实际效果 |
|---|---|---|
| `01-KAIRO-VOSS-霓虹青蓝球体作品集.html` | KAIRO VOSS | 深空蓝黑底 + 青蓝霓虹，右侧一颗带线框经纬的发光变形球体，中心向四周溢光；左侧编辑式大标题，横向 SCROLL / DRAG 滑动 7 屏作品集 |
| `02-GLOW-金色恒星发光球体.html` | GLOW | 纯黑底上一颗金色恒星：亮核、光环、放射状光线与星点尘埃，十字准星鼠标，底部 MOVE / SCROLL / CLICK 交互提示 |
| `03-HEXFORGE-熔核蜂巢矩阵控制台.html` | HEXFORGE // 熔核蜂巢矩阵 | 近黑琥珀底，六边形蜂巢晶格与熔核辉光（WebGL），叠加 HUD 扫描线、菱形括角与右下角 FORGE CONTROL 滑杆面板 |
| `04-KILN-熔金余烬粒子作品集.html` | KILN | 深褐底满屏橙红余烬粒子漂浮，衬线大字斜体渐变标题（Molten Chorus），左侧 01–06 目录，底部 6 张折叠缩略图导航 |
| `05-KAI-荧光波形信号作品集.html` | KAI | 纯黑底 + 荧光黄绿，右侧一块实时波形示波面板（双曲线 + 网格），等宽字体按钮，网格暗纹，工程感信号美学 |
| `06-知微ZHWEI-中文大模型品牌页.html` | 知微 ZHWEI | 米色宣纸底 + 朱红，右侧巨大「知微」书法字与印章，左侧「见微，知著」中文黑体排版，东方极简品牌页 |
| `07-SOLSTICE-黄金时刻极光信息流.html` | SOLSTICE | 橙金渐变社交信息流：顶部搜索框、一排极光头像环、瀑布流卡片（MOTION / AI 标签、点赞与音量条）、底部悬浮 dock |
| `08-SOLIDUS-体积等值面工作站.html` | SOLIDUS · 体积等值面工作站 | WebGPU GPU Marching Cubes 体渲染工作站：数据集体（Gyroid / 小行星 / 电子轨道 / 松质骨 / 机械齿轮）、体素分辨率与 .raw 载入控制台 |
| `09-AURELIAN-ORBIT-GPU音视觉粒子球体.html` | AURELIAN // ORBIT | 深棕金氛围，中央悬浮金色粒子球体（序列帧粒子集），大字标题 + CLICK TO ENGAGE，底部音轨信息与播放进度，GPU 程序化作曲音视觉 |
| `10-VESPER-实时3D实验作品集.html` | VESPER | 纯黑底，首屏为「Press and hold anywhere to begin a tutorial」持按教程遮罩；跳过或长按后进入 REALTIME OBJECTS IN MOTION，霓虹青绿渐变标题 + 6 个 WebGL 实验模块卡片 |

### 环境相关说明

- `08` 需要 WebGPU，`10` 部分模块需要 WebGL：在不支持的环境会显示「无法获取 GPU 适配器」提示页，属正常降级。
- `03` 在无 GPU 的软件渲染（SwiftShader）下，整屏可能被刷白：这是 `THREE.LineSegments` 线光栅化的环境假象，不是页面缺陷，真机独显下正常。

## 使用

无需安装依赖，双击任意 `.html` 文件即可在浏览器中打开：

```bash
# 或者用任意静态服务器（可选）
python -m http.server 8000
# 然后访问 http://localhost:8000/01-KAIRO-VOSS-霓虹青蓝球体作品集.html
```

## 技术说明

- 单文件架构：每个作品独立为一个 HTML 文件，内联全部样式与脚本
- 渲染技术：Canvas 2D、WebGL、WebGPU（按作品）
- 无外部 CDN 依赖（或仅有少量字体/库引用，见各文件源码）
