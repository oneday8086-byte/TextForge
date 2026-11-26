# ⚒️ TextForge

> **A minimalist, high-performance Swiss Army Knife for text, JSON, and XML parsing.**  
> 一款极简、高效的文本与数据格式转换/预览瑞士军刀。

[![Made with AI](https://img.shields.io/badge/Made%20with-AI%20Pair%20Programming-blueviolet.svg)](#-开发故事--致谢)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen.svg)](#)

TextForge 是一个单文件的纯前端 Web 工具，专为开发者设计。它不仅能自动将字面量转义字符（如 `\n`, `\t`）解析为真实的换行，还能实时预览 Markdown，并提供可交互、可编辑的 JSON 与 XML 树状视图。

## ✨ 核心特性 (Features)

- **🪄 转义文本解析**：一键将 `\n`、`\t`、`\uXXXX` 等字面量转义符替换为真实换行与空格，告别从日志或代码中复制粘贴时的排版混乱。
- **📝 Markdown 实时预览**：支持 GFM 规范，边写边看，自带 HTML 净化（DOMPurify），安全可靠。
- **🌲 交互式 JSON 树形视图**：
  - 支持超大型 JSON 的**虚拟滚动**，丝滑不卡顿。
  - 支持层级**折叠/展开**。
  - **行内双击编辑**：直接在预览区双击修改 Value 值，自动同步回原始文本。
  - 一键**格式化（Beautify）**与**压缩（Minify）**。
- **📄 XML 解析与互转**：
  - 完美支持 XML 的格式化与单行压缩。
  - 自动解析 XML 结构并转换为 JSON 树形视图查看。
  - 在 JSON 视图中编辑后，自动反向生成合法的 XML 源码！
- **🎨 现代 UI 体验**：支持深色/浅色主题无缝切换、双栏同步滚动、拖拽调整面板宽度。
- **📦 零依赖单文件**：整个工具就是一个 `.html` 文件，无需构建，随处运行。

## 🚀 快速开始 (Getting Started)

### 方式一：直接使用（推荐）
1. 下载本项目的 `index.html`。
2. 双击在浏览器中打开即可使用。
3. （可选）如果你希望完全离线且不依赖任何外网 CDN，请将 `marked` 和 `DOMPurify` 的 `.min.js` 文件下载到本地 `lib/` 目录，并修改 HTML 中的 `<script>` 引用路径。

### 方式二：本地开发
由于是纯静态单文件项目，你可以使用任何本地静态服务器运行：

```bash
# 使用 Python
python -m http.server 8080

# 或使用 Node.js (http-server)
npx http-server .
```

## 🌐 在线体验 & 部署 (Demo & Deployment)

本项目非常适合部署在各类免费的静态托管平台：
- **腾讯云 EdgeOne Pages** (推荐，国内访问速度极佳)
- **GitHub Pages** (适合作为开源项目展示)
- **Cloudflare Pages / Vercel** 等。

> **部署建议**：如果部署在国内平台（如 EdgeOne），建议将外部 CDN 依赖（marked, purify）本地化，以确保 100% 的可用性。

## 🛠️ 技术栈 (Tech Stack)

- **HTML5 / CSS3 / Vanilla JavaScript** (无框架依赖，极致轻量)
- **[marked](https://github.com/markedjs/marked)**: 极速 Markdown 解析。
- **[DOMPurify](https://github.com/cure53/DOMPurify)**: 强大的 XSS 防护与 HTML 净化。
- **虚拟滚动 (Virtual Scrolling)**：原生 JS 实现，专为海量数据优化渲染性能。

---

## 🤖 开发故事 & 致谢 (Acknowledgments)

这个项目的诞生非常有趣：**这里 100% 的代码都是由 AI 编写的。**

整个开发过程采用了“人类产品经理 + AI 程序员”的结对编程模式：
*   人类负责提需求：“我要转义解析”、“加个 JSON 编辑器”、“支持一下 XML”、“输入框太窄了改宽点”、“压缩功能报错了修一下”……
*   AI 负责疯狂输出代码、修复 Bug、完善虚拟滚动算法，并且在你打字问问题的时候，乖巧地回答：“好的，这是修改后的完整代码。”

特别感谢 [DeepSeek](https://www.deepseek.com/) 提供的强大代码生成与上下文理解能力，让这个纯手工打磨的单文件工具成为了可能。

*(人类开发者的唯一特权：在键盘上敲下 `Ctrl + C` 和 `Ctrl + V`，以及回复“666666，给你点赞”。)*

---

## 📄 开源协议 (License)

[MIT License](LICENSE) © TextForge