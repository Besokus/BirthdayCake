# BirthdayCake · Luxury 3D Birthday Cake

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 项目简介

BirthdayCake 是一个基于 WebGL 的沉浸式 3D 生日蛋糕网页，支持上传照片、音乐和祝福文字，通过手势与场景互动，打造高质感的生日祝福体验。  
只需一个 HTML 文件和现代浏览器，即可本地运行或部署到任意静态网站托管平台（例如 GitHub Pages）。

## 功能特性

- 3D 豪华生日蛋糕场景，支持发光、景深与光晕等效果
- 支持上传背景音乐（MP3 等常见格式），实现个性化 BGM
- 支持上传照片，将照片以相框形式展示在蛋糕周围
- 支持撰写与展示“生日书信”，以毛笔风格字体呈现
- 支持导入 / 导出配置（JSON），便于保存与分享场景
- 支持全屏浏览，适合大屏展示与仪式感场景
- 集成 MediaPipe 手部识别，可基于手势进行交互（如旋转视角等）
- 纯前端实现，无需后端服务，易于部署

## 安装指南

### 环境要求

- 现代桌面浏览器：推荐使用最新版本的 Chrome / Edge
- 设备需具备：
  - 可访问互联网（用于加载 three.js 与 MediaPipe CDN 资源）
  - 可选：带摄像头的设备（用于手势识别与交互）

### 获取源码

使用 Git 克隆仓库：

```bash
git clone https://github.com/你的用户名/BirthdayCake.git
cd BirthdayCake
```

或直接在 GitHub 上下载 ZIP 并解压。

### 依赖安装

本项目为纯静态页面，核心依赖通过 CDN 在线加载，无需本地安装 NPM 包或构建工具：

- three.js（3D 渲染）
- @mediapipe/tasks-vision（手部关键点识别）

如果你希望在离线环境下使用，可以将相关依赖下载到本地并修改 `Birthdaycake.html` 中的 `importmap` 地址。

## 使用说明

### 本地打开

#### 方式一：直接用浏览器打开

1. 在文件管理器中找到 `Birthdaycake.html`
2. 使用 Chrome / Edge 打开该文件  
   若出现浏览器安全限制（部分浏览器限制 `file://` 加载模块），请使用下一种方式。

#### 方式二：使用本地静态服务器（推荐）

在项目目录下使用任意静态服务器，例如：

```bash
# Python 3
python -m http.server 8000

# 或使用 Node.js 的 serve（需提前全局安装）
npx serve .
```

然后在浏览器中访问：

```text
http://localhost:8000/Birthdaycake.html
```

### 页面交互说明

打开页面后，你将看到加载动画以及 3D 生日蛋糕场景，右上角提供多个操作按钮：

- `上传音乐`：选择本地音乐文件作为背景音乐
- `上传照片`：选择一张或多张本地图片，展示在蛋糕周围的相框中
- `上传书信`：打开书信编辑弹窗，撰写你的祝福文字
- `导入网页`：从 JSON 文件导入之前导出的场景配置
- `导出网页`：导出当前场景配置为 JSON 文件，方便备份或分享
- `全屏显示`：切换到全屏模式，适合仪式感展示

如需使用手势交互：

1. 确保浏览器已允许摄像头权限
2. 在页面右下角可以看到摄像头预览区域
3. 按提示使用手势在空中做出动作，即可与场景产生互动（例如旋转观察蛋糕）

## 示例与截图

你可以在准备部署之前添加自己的截图，例如：

```markdown
![示例界面](./docs/screenshot.png)
```

请将 `./docs/screenshot.png` 替换为你实际的截图路径，并将图片文件加入仓库。

## 贡献指南

欢迎对 BirthdayCake 提出改进与新功能建议。你可以通过以下方式参与：

- 提交 Issue：反馈 Bug、提出新功能或改进建议
- 提交 Pull Request：  
  - Fork 本仓库
  - 创建新分支进行开发（例如：`feature/add-new-effect`）
  - 确保本地在主流浏览器中测试通过
  - 提交 PR 并说明改动内容与动机

在提交代码时，建议：

- 保持代码风格与现有实现一致（例如命名与缩进风格）
- 避免引入不必要的大型依赖，优先使用原生或现有库

## 许可证

本项目基于 MIT 许可证开源发布。  
详情请参阅仓库中的 [LICENSE](./LICENSE) 文件。

