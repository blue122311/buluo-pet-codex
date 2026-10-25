# 来源、署名与许可

## 上游桌宠项目

- 原项目：[PC2005-cloud/dsh-pet](https://github.com/PC2005-cloud/dsh-pet)。
- 原作者：**PC2005-cloud**。
- 适配的上游基线：[`e17e89be92aaa7b71c4f3e9e89995a23a781d725`](https://github.com/PC2005-cloud/dsh-pet/tree/e17e89be92aaa7b71c4f3e9e89995a23a781d725)。
- 原代码采用 MIT，保留 `Copyright (c) 2026 PC2005-cloud` 及完整许可正文，见 [LICENSE](LICENSE) 和 `dsh-pet/LICENSE`。

桌宠运行核心、动画播放、桌面渲染、拖拽交互及相关实现来自上游。本仓库由 **blue122311 与不落**在此基础上加入 Codex 插件设置、本机会话状态读取、可选碎碎念及 Windows 安装分发。这是独立维护的社区适配版本。

上游 [README 的许可说明](https://github.com/PC2005-cloud/dsh-pet/blob/e17e89be92aaa7b71c4f3e9e89995a23a781d725/README.md#%E8%AE%B8%E5%8F%AF) 区分代码与素材：代码为 MIT；动画、提示词和源视频允许开源使用、禁止商用，并要求衍生、改版、换皮作品在介绍、展示和分发处附原作者仓库地址。转载本适配版时，请继续保留原作者链接、版权及许可说明，不将整个项目的素材一并标作 MIT。

## “不落”角色与动画

本次附带的“不落”角色与 24 段动画是 **blue122311 与不落**自己的角色内容和成品，保存在 `pet-content/pet/buluo-drawn-animation/`，与上游默认角色动画分别归属。

这些成品此次仅作公开分享，未另行授予素材许可证，也未置于上游代码的 MIT 许可下。请保留来源署名；需要转载、修改或另作分发时，请先联系仓库维护者确认素材授权。

本次不分发上游默认 106 段角色动画、上首软糖体字体或上游表情包，也不将这些内容记作本仓库原创。文字显示使用系统字体回退。

## 随包运行环境

0.3.0 Windows x64 完整包附带以下运行时及原许可文件：

| 组件 | 版本与来源 | 保留的许可文件 |
| --- | --- | --- |
| Node.js | 24.21.0，[Node.js 官方项目](https://nodejs.org) | Node.js `LICENSE` |
| Electron | 43.3.0，[electron/electron](https://github.com/electron/electron) | Electron `LICENSE`、`LICENSES.chromium` |

打包使用的运行时来自本机已有的上游原生分发副本，版本已读取核对。随包保留上述原许可证及第三方声明，不因本仓库代码采用 MIT 而改变它们的许可。

其他运行与构建依赖沿用各自原许可证，具体版本见包清单、锁文件及源码归档 `source-code-0.3.0.zip`。Windows 完整包另行提供，文件名为 `buluo-pet-codex-0.3.0-windows-x64.zip`。

公开包不包含个人登录、聊天记录或正式记忆。Codex 是 OpenAI 的产品；本仓库提供社区适配，不代表 OpenAI、DeepSeek 或原桌宠作者的官方支持。
