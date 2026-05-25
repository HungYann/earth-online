# 🌍 EARTH ONLINE

一个实时 3D 地球可视化项目，展示全球航班动态、昼夜分布与大气层效果。

**在线预览：** [https://video-mu-wine.vercel.app/](https://video-mu-wine.vercel.app/)

---

## 功能特性

- **3D 地球渲染** — 基于 Three.js，含昼夜纹理、大气层散射、云层动画
- **全球航班** — 模拟 50 架航班分布于主要国际航线，✈ emoji 图标按高度分色
- **航班点击互动** — 点击飞机展示航班信息卡（航班号、机型、速度、高度、航向），附脉冲光环动画与每日随机情绪语
- **实时时钟** — 显示 UTC+8 时间
- **每日一语** — 每天自动更换一句旅行随想，30 句循环
- **图层控制** — 可独立开关云层、航班显示

## 技术栈

- [Three.js r160](https://threejs.org/) — WebGL 3D 渲染
- GLSL 自定义着色器 — 地球昼夜混合、大气层边缘光
- OrbitControls — 鼠标拖拽旋转、缩放、自动旋转
- 纯 HTML 单文件，无构建工具依赖
- 部署于 [Vercel](https://vercel.com/)

## 本地运行

直接用任意静态文件服务器打开 `earth-online.html`，例如：

```bash
npx serve .
```

然后访问 `http://localhost:3000`。

## 文件结构

```
earth-online.html        # 主文件（全部逻辑含于此）
flights_2026-05-25.json  # 示例航班数据（aviationstack 格式）
vercel.json              # Vercel 部署配置
```

## 数据来源

- 地球纹理：[webgl-earth](https://github.com/turban/webgl-earth)（NASA 公开图像）
- 航班数据：本地 JSON 示例 + 内置模拟生成（覆盖全球主要航线）
