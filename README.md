# 不落桌宠 · Codex 适配版

基于 [PC2005-cloud/dsh-pet](https://github.com/PC2005-cloud/dsh-pet) 的桌宠运行核心，为 Codex 增加插件设置和任务状态联动，附带“不落”角色的 24 段透明动画成品。

原桌宠项目由 **PC2005-cloud** 开发；本仓库的 Codex 适配及“不落”角色内容由 **blue122311 与不落**整理维护。感谢原作者开放源码。完整来源与许可见 [ATTRIBUTION.md](ATTRIBUTION.md) 和 [LICENSE](LICENSE)。

**版本：0.2.2。这是按现有运行方式整理的源代码快照。** 原生任务联动需要另行准备 `billion-context-runtime` 宿主；本仓库不分发该宿主，也不承诺仅安装普通 Codex 就能直接使用。尚未在另一台电脑上完成动态安装验收。

## 可以做什么

- 在插件设置中调整桌宠名字、大小、位置、显示和动作。
- 播放待机、思考、书写、走路、拖拽等角色动画。
- 通过已有原生宿主接收 Codex 任务状态，切换对应动作。
- 按需启用碎碎念；配置外部记忆系统后，可选择绑定主会话或跟随任务读取上下文。

碎碎念和上下文读取默认关闭。原生状态联动与记忆接续是两个独立接入：只需要状态动作时，可以不配置记忆系统。

## 环境与安装

目前按 Windows 环境整理，需要 Node.js 22.12.0 或更新版本、npm，以及已经可用的 `billion-context-runtime` 原生宿主实现。记忆接续另外需要已有的 `memory-system` 及其 Python 环境。

本仓库通过归档提供完整源码。请到 [v0.2.2 下载页](https://github.com/blue122311/buluo-pet-codex/releases/tag/v0.2.2) 下载 `buluo-pet-codex-0.2.2.zip`；它同时包含源码、配置和全部 24 段动画。仓库根目录的 `source-code-0.2.2.zip` 是便于阅读和研究的纯源码归档，不包含动画，不能单独用于安装。

在 PowerShell 中解压完整包并构建：

```powershell
Expand-Archive -LiteralPath .\buluo-pet-codex-0.2.2.zip -DestinationPath .\buluo-pet-codex
cd buluo-pet-codex
npm ci --legacy-peer-deps
npm ci --prefix dsh-pet --legacy-peer-deps
npm run build --prefix dsh-pet
```

配置本机路径。以下路径仅为示例，请替换成自己已准备好的实际目录：

```powershell
node scripts/setup.mjs --native-host-root "C:\tools\billion-context-runtime"
node scripts/download-electron.mjs
```

需要记忆接续时，在配置中额外传入记忆系统目录：

```powershell
node scripts/setup.mjs --native-host-root "C:\tools\billion-context-runtime" --memory-root "C:\tools\memory-system"
```

`setup` 默认保留已有本地设置，生成个人路径配置和 `.trial` 运行目录。它不会替你安装或启动外部原生宿主、搭建记忆系统。

本地插件入口是 `codex-plugin/.codex-plugin/plugin.json`，对应的 `.mcp.json` 由 `setup` 生成。依照 [OpenAI 官方插件构建与手动安装说明](https://developers.openai.com/plugins/build/plugins) 在自己的 Codex 中加载本地插件，再从插件设置控制桌宠。这里提供的是手动源码适配方式。

完成本机配置后，在仓库根目录将它添加为本地插件源：

```powershell
codex plugin marketplace add .
```

再在桌面端插件目录中选择“不落桌宠 · 社区适配”来源，安装“不落桌宠”。本地源的配置与准备步骤需要先执行；这不是官方通用插件目录上架。

## 可选的碎碎念与记忆接续

碎碎念代码保留现有的 Codex 登录调用：只读本机现有登录，不刷新或回写凭据；模型为 `gpt-6-luna`，推理强度为 `max`。实际账号是否能够调用该模型，以账号和服务端当时的支持为准。

启用上下文接续后，相关聊天和记忆由你配置的外部 `memory-system` 在本机准备，再用于碎碎念生成。请先确认自己的接入路径和读取范围。`setup` 生成的路径配置、`.trial`、登录凭据、聊天记录及个人记忆属于本地数据，不要提交到公开仓库。

## 仓库内容与许可

| 内容 | 说明 |
| --- | --- |
| `dsh-pet/` | 上游桌宠运行核心及本地适配，保留原 MIT 许可和版权声明 |
| `codex-plugin/` | Codex 插件入口、设置与状态接入 |
| `scripts/` | 源码快照的本机配置与运行依赖准备入口 |
| `pet-content/pet/buluo-drawn-animation/` | “不落”角色的 24 段透明动画成品 |

本次不附带上游默认 106 段动画、上首软糖体字体或上游表情包；文字显示使用系统字体回退。上游动画、提示词和源视频有独立的非商用及署名约定，不能因为代码采用 MIT，就将这些素材一并标作 MIT。

“不落”角色与动画此次仅作公开分享，未另行授予素材使用许可证。代码许可证不自动适用于这些原创素材；具体来源与范围见 [ATTRIBUTION.md](ATTRIBUTION.md)。
