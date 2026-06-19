# 💣 Material 3 扫雷

> 一个用 **Google Material Design 3** 设计语言重写的单文件扫雷游戏，零依赖、零安装、浏览器双击即玩。

## 🎮 立即试玩

**[👉 在线试玩 (GitHub Pages)](https://cizuwuxin.github.io/saolei/saolei.html)**

支持电脑、手机、平板，自动适配深色 / 浅色主题。

---

## ✨ 特性

- 🎨 **Material 3 设计语言** — 完整 Material You 配色 token 系统，浅色 / 深色主题无缝切换
- 🧠 **智能无猜模式** — 内置 **CSP 约束传播求解器**（变量消元 + 组件分析），自动识别能确定安全的格子
- ⚡ **Web Worker 并行池** — 求解器在多核 CPU 后台并行跑，不卡 UI
- 🛡️ **首次点击保护** — 第一次点击一定是安全的
- ↩️ **撤销系统** — 最多保留 50 步操作历史
- 📊 **记录与统计** — 各级别最佳成绩持久化
- ⌨️ **键盘 + 触屏** — 鼠标、长按、双击、数字键插旗 / 展开都支持
- 🎬 **动画系统** — 翻格 / 插旗 / 爆炸 / 胜利都有过渡动画
- 📱 **完全响应式** — 从 360px 手机到 4K 显示器自适应布局

## 🚀 使用

### 在线玩
直接访问 https://cizuwuxin.github.io/saolei/saolei.html

### 本地玩
1. 克隆仓库或下载 `saolei.html`
2. 双击文件，浏览器打开即可

```bash
git clone https://github.com/cizuwuxin/saolei.git
# 然后用浏览器打开 saolei.html
```

### 自己托管
文件完全自包含，扔到任何静态服务器都行：
- **Vercel / Netlify**：拖进项目目录，自动部署
- **Cloudflare Pages**：连 git 仓库，30 秒上线
- **自己的服务器**：`python3 -m http.server 8080`

## 🕹️ 操作说明

| 操作 | 鼠标 | 触屏 | 键盘 |
|---|---|---|---|
| 翻开格子 | 左键单击 | 轻点 | 方向键移动 + Enter |
| 标记地雷 | 右键单击 | 长按 | F 键 |
| 数字展开 | 双击数字 | 双击数字 | 双击数字 / 长按数字 |
| 切换主题 | 顶栏按钮 | 顶栏按钮 | — |
| 撤销 | 顶栏按钮 | 顶栏按钮 | Ctrl+Z |

## 🏆 难度

| 难度 | 尺寸 | 地雷 |
|---|---|---|
| 简单 | 9 × 9 | 10 |
| 中等 | 16 × 16 | 40 |
| 困难 | 16 × 30 | 99 |
| 自定义 | 自由 | 自由 |

## 🧩 技术亮点

- **CSP 求解器**：把扫雷建模为约束满足问题（Constraint Satisfaction Problem），通过变量消元 + 组件分析找出能确定的位置
- **Web Worker 池**：根据 `navigator.hardwareConcurrency` 自动调整 worker 数量
- **Material 3 token 系统**：`--md-sys-color-*` 完整配色，支持 `color-mix(in srgb, ...)` 现代语法
- **撤销系统**：`Uint8Array` 扁平化快照 + 栈结构，O(1) 还原
- **零依赖**：不引任何外部库，整个游戏就一个 HTML 文件

## 🛠️ 自定义

打开浏览器 DevTools → 改 CSS 变量即可换主题色：

```css
:root {
  --md-sys-color-primary: #6750A4;   /* 改成你喜欢的颜色 */
  --md-sys-color-secondary: #625B71;
}
```

## 📜 许可证

[MIT](./LICENSE) — 随便用、商用、改、私有部署都行，保留原作者声明即可。

## 🌟 Star History

如果这个项目让你玩得开心，欢迎点 ⭐ Star 让更多人看到！

## 🤝 贡献

欢迎提 Issue / PR：
- 新的难度模式
- 新的关卡机制
- 新的视觉主题
- 性能优化
- Bug 修复

---

Made with 💜 by [cizuwuxin](https://github.com/cizuwuxin)
