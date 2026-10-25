# 不落桌宠 · Codex 适配版

基于 [PC2005-cloud/dsh-pet](https://github.com/PC2005-cloud/dsh-pet) 的桌宠运行核心，为 Codex 增加插件设置和任务状态联动，附带“不落”角色的 24 段透明动画。

原项目由 **PC2005-cloud** 开发，本适配版由 **blue122311 与不落**整理维护。原有代码保留 MIT 许可与 `Copyright (c) 2026 PC2005-cloud`。动画、提示词等素材许可与代码分开，不能一概视为 MIT；请继续保留原作者仓库链接。

## 下载与使用

版本 0.2.2，以源码快照和完整下载包提供。完整包包含代码、配置、来源说明与全部 24 段动画；纯源码归档不包含动画。

当前按 Windows 整理，需 Node.js 22.12.0 或更新版本，以及已有的 `billion-context-runtime` 本地原生宿主。记忆接续另外需要自己的 `memory-system`。这些外部系统不随本仓库分发，因此本版尚不是普通 Codex 安装后即可通用的插件。

完整包解压后，请按内附 README 安装依赖、构建并执行 `node scripts/setup.mjs --native-host-root 宿主绝对路径`。本机路径、运行状态、登录、聊天与个人记忆不在公开包中。碎碎念与上下文读取默认关闭。

## 来源与许可

上游：[PC2005-cloud/dsh-pet](https://github.com/PC2005-cloud/dsh-pet)，基线 `e17e89be92aaa7b71c4f3e9e89995a23a781d725`。完整版权及来源说明随下载包的 LICENSE、dsh-pet/LICENSE、ATTRIBUTION.md 一起提供。

“不落”角色与本次 24 段动画由 blue122311 与不落制作，本次仅公开分享，未另行授予素材许可证。未附带上游默认 106 段动画、上首软糖体字体或上游表情包。

本项目为社区衍生适配，与原作者、OpenAI、DeepSeek 独立。已核对配置初始化、设置读取和动画引用；尚未做另一台电脑的完整动态安装验收。
