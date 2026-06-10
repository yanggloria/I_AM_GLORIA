# I AM GLORIA

这是从单个 HTML 文件整理出的静态前端项目。整理时保留了原页面的文字、视觉效果和交互逻辑，没有改写成 React/Vue 等框架项目。

## 项目结构

```text
I_AM_GLORIA/
├─ index.html
├─ css/
│  └─ style.css
├─ js/
│  └─ main.js
├─ assets/
│  └─ .gitkeep
├─ backup/
│  └─ original.html
├─ I_AM_GLORIA.html
├─ README.md
└─ .gitignore
```

## 文件说明

- `index.html`：整理后的入口文件，可以直接双击打开。
- `css/style.css`：从原始 `<style>` 拆分出的样式文件。
- `js/main.js`：从原始内联 `<script>` 拆分出的交互脚本。
- `backup/original.html`：原始 HTML 备份。
- `I_AM_GLORIA.html`：根目录下保留的原始文件，方便对照。
- `assets/`：预留给后续图片、字体、音频、视频等资源。

## 外部 CDN

项目保留了原始 HTML 中的外部 CDN 链接：

- `https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js`
- `https://cdn.jsdelivr.net/npm/@mediapipe/hands/hands.js`
- `https://cdn.jsdelivr.net/npm/@mediapipe/camera_utils/camera_utils.js`

这些链接用于 3D 渲染和手势识别。离线或网络不可用时，相关功能可能无法加载。

## 本地资源备注

原始页面中引用了以下本地 PWA 资源，但当前文件夹里没有对应文件：

- `manifest.webmanifest`
- `icons/icon-192.png`
- `sw.js`

这些引用已保留，避免改变原页面行为。双击 `index.html` 时，Service Worker 不会在 `file://` 协议下注册；如果以后要完整启用 PWA，可补齐这些文件或再调整路径。

## 使用方式

直接双击 `index.html` 即可打开页面。部分摄像头/手势功能可能需要浏览器授权，并且在 `localhost` 或 HTTPS 环境下兼容性更好。
