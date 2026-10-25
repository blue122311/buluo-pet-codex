# 来源、署名与许可

## 上游桌宠项目

- 原项目：[PC2005-cloud/dsh-pet](https://github.com/PC2005-cloud/dsh-pet)。
- 原作者：**PC2005-cloud**。
- 本次适配的上游基线：[`e17e89be92aaa7b71c4f3e9e89995a23a781d725`](https://github.com/PC2005-cloud/dsh-pet/tree/e17e89be92aaa7b71c4f3e9e89995a23a781d725)。
- 原代码许可：MIT，版权行为 `Copyright (c) 2026 PC2005-cloud`；完整正文随附于仓库 [LICENSE](LICENSE) 及 `dsh-pet/LICENSE`。

原有桌宠运行核心、动画播放、桌面渲染、拖拽交互及相关实现来自上游。本仓库在此基础上加入 Codex 插件设置、原生任务状态接入及相关本地适配，由 **blue122311 与不落**整理维护；这是独立的衍生适配版本。

原上游 [README 的许可说明](https://github.com/PC2005-cloud/dsh-pet/blob/e17e89be92aaa7b71c4f3e9e89995a23a781d725/README.md#%E8%AE%B8%E5%8F%AF) 将代码与素材分开：代码采用 MIT；动画、提示词及源视频允许开源使用、禁止商用，并要求衍生、改版、换皮作品在介绍、展示、分发处附原作者仓库地址。转载本适配版时，请继续保留原作者链接、版权和许可说明，不把整个项目的素材笼统标成 MIT。

## “不落”角色与动画

“不落”角色及本次附带的 24 段动画是 blue122311 与不落自己的角色内容和成品，保存在 `pet-content/pet/buluo-drawn-animation/`，与上游默认角色动画分别归属。

本次仅公开分享这些成品，未另行授予素材许可证，也未将它们置于上游代码的 MIT 许可下。请保留来源署名；需要转载、修改或另作分发时，请先联系仓库维护者确认素材授权。

## 未随本快照分发的内容

本次不附带上游默认 106 段角色动画、上首软糖体字体或上游表情包。字体显示使用系统字体回退。本仓库没有为这些未分发素材重新授予许可证，也不将它们记作本仓库原创。

原生任务联动依赖外部 `billion-context-runtime`，记忆接续依赖外部 `memory-system`；这两个系统不在本仓库内分发，其存在及接入方式不构成对其代码或数据的再许可。公开包不包含个人登录、聊天记录和正式记忆。

## 第三方运行与构建依赖

项目使用 Node.js、Electron、React、DeepSeek Harness 相关模块及包清单列出的构建工具。依赖的具体版本见 `package.json`、`dsh-pet/package.json` 及对应锁文件；这些依赖沿用各自原许可证。安装时从相应软件源获取的依赖，不因本仓库的 MIT 代码许可改变原有许可。

Codex 是 OpenAI 的产品。本仓库提供社区适配，不代表 OpenAI、DeepSeek 或原桌宠作者的官方支持。
