# WarmLabel / 暖言纸条

> A small, warm space for writing, receiving, and keeping kind words.
> 一个记录、传递和收藏温暖话语的小空间。

WarmLabel was created as a Microsoft Imagine Cup project. It is a cross-platform mobile application prototype built with uni-app/Vue and supported by a Flask backend.

暖言纸条是一个微软 Imagine Cup 项目，目标是通过简单、友好的交互，让用户写下暖言、接收暖言，并在日常生活中获得持续的情绪支持。目前项目以跨平台移动端原型为主，使用 uni-app/Vue 构建前端，并由 Flask 后端提供基础服务。

## Features / 功能

### Warm messages / 暖言

- Write and send a warm message with a simple editor.
- Receive a warm message and respond with a return message.
- Limit message content to a practical length for short, focused expressions.

- 编写并发送暖言。
- 接收暖言，并通过“回礼”传递回应。
- 为内容设置长度限制，鼓励简短、真诚、聚焦的表达。

### Personal notes / 个人笔记

- Create notes with a title and body.
- Record the current emotion with positive, neutral, or unhappy mood options.
- Record and play back an optional voice note.
- Browse the notebook and access note-related views.

- 创建带标题和正文的笔记。
- 选择当前情绪，包括开心、一般和不开心等状态。
- 录制并播放可选的语音内容。
- 浏览个人笔记本及相关页面。

### History, music, and store / 历史、音乐与商店

- View previously displayed warm-message history.
- Play relaxing background music and pause or resume playback.
- Explore the in-app store concept and its virtual currency interface.
- Navigate between the home page, settings, and music pages.

- 查看历史暖言。
- 播放、暂停和继续背景音乐。
- 浏览商店概念页面及虚拟货币界面。
- 在首页、设置和音乐页面之间切换。

### Account and backend services / 账号与后端服务

- Register and log in with a username, email, and password.
- Store passwords as hashes rather than plain text.
- Use JWT access tokens for authenticated requests.
- Provide profile and health-check API endpoints.

- 使用昵称、邮箱和密码注册、登录。
- 以哈希形式保存密码，不直接保存明文密码。
- 使用 JWT 访问令牌进行身份认证。
- 提供个人资料和健康检查接口。

## Project structure / 项目结构

```text
.
├── uniapp_vue_main/       # uni-app/Vue mobile frontend / 移动端前端
│   ├── pages/             # Application pages / 页面
│   ├── static/            # Images, icons, and styles / 图片、图标与样式
│   └── manifest.json      # uni-app application configuration / 应用配置
├── python_flask/          # Flask backend / Flask 后端
│   ├── main.py            # API server and database models / API 服务与数据模型
│   ├── test_api.py        # Backend tests / 后端测试
│   ├── pyproject.toml     # Python dependencies / Python 依赖
│   └── .env.example       # Environment variable template / 环境变量模板
└── README.md
```

## Getting started / 快速开始

### Backend / 后端

The backend requires Python 3.13 or newer.

后端需要 Python 3.13 或更高版本。

```bash
cd python_flask
cp .env.example .env
python main.py
```

The Flask service listens on port `5000` by default. It exposes the root status page at `/`, health checks at `/api/health`, and account endpoints under `/api`.

Flask 服务默认监听 `5000` 端口：`/` 用于查看服务状态，`/api/health` 用于健康检查，账号相关接口位于 `/api` 下。

### Frontend / 前端

Open `uniapp_vue_main` with HBuilderX or another compatible uni-app development environment, then run the application on a simulator or supported mobile platform.

使用 HBuilderX 或其他兼容 uni-app 的开发环境打开 `uniapp_vue_main`，然后在模拟器或支持的平台上运行应用。

> The frontend currently contains prototype screens and some demonstration data. Backend integration for every screen is still in progress.
> 当前前端部分页面仍属于原型或演示状态，并非所有页面都已完成后端联调。

## Roadmap / 未来更新计划

- **Model migration / 切换模型**
  Replace the current model or model integration with a more capable, reliable, and cost-effective option as the product requirements become clearer.

  根据产品需求，切换到能力更强、更稳定且成本更合适的模型或模型接入方案。

- **AI Agent review for warm messages / 使用 AI Agent 审查暖言**
  Add an AI Agent review pipeline for submitted warm messages. The Agent will help identify harmful, discriminatory, harassing, unsafe, or otherwise inappropriate content before publication, while keeping human control and clear explanations for review results.

  为提交的暖言增加 AI Agent 审查流程，在发布前辅助识别伤害性、歧视性、骚扰性、不安全或其他不合适的内容，同时保留人工控制，并对审查结果提供清晰说明。

- **Complete product integration / 完善产品联调**
  Connect note, history, store, music, and warm-message flows to persistent backend data and improve error handling, permissions, and mobile usability.

  将笔记、历史、商店、音乐和暖言流程接入持久化后端数据，并完善错误处理、权限管理与移动端体验。

## License / 许可证

No license has been selected yet. Add a license file before distributing the project publicly.

目前尚未选择开源许可证。如需公开分发项目，请先补充许可证文件。
