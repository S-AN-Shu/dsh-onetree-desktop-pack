# DSH Desktop 增强配置包

适用 **Windows x64 上的 DeepSeek Harness Desktop 0.2.0-rc.2**，组合阅读界面、进度播报、ACP 认知压缩、持久记忆等 20 个插件组件。

## 安装

1. 在 [v0.1.2 Release](https://github.com/S-AN-Shu/dsh-onetree-desktop-pack/releases/tag/v0.1.2) 下载 ZIP 并解压。
2. 打开 Desktop「插件 → 添加插件」，输入主文件 `dsh-onetree-desktop-pack-0.1.2.tgz` 的绝对路径，安装后选择「立即启用」。
3. 在新会话中选择「ACP 认知压缩 · 标准 / PTC / 精简 / Cordis」。

也可直接导入主 TGZ 的 [公开下载地址](https://github.com/S-AN-Shu/dsh-onetree-desktop-pack/releases/download/v0.1.2/dsh-onetree-desktop-pack-0.1.2.tgz)。ZIP 用于下载，实际导入格式为 TGZ；主包已内置组件，避免 URL 子依赖的安装限制。不要分别启用组件再启用主包。

## 预设与首次使用

四个增强预设分别保留标准、PTC、精简、Cordis 运行模式，接入一个 ACP 和持久记忆实例。它们不是模型，使用安装者自己的模型配置；原有预设仍可使用，并不会自动切换到 ACP。

模型账户自行配置。记忆从空存储开始，需要 Python 3.9+ / PyYAML；Argo 仍需其公共后端及系统 Node/npm。Blender、代理和 WSL 扩展默认未启用，需要时填写自己的环境配置；PTC 是独立运行模式。提示词设置默认关闭，没有附加协作人设。

组件与版本见 [CONTENTS.json](CONTENTS.json)，验证范围和完整性见 Release 的 `VALIDATION.json` 与 `SHA256SUMS.txt`。配置采用 MIT，各组件及内置依赖保留原许可；来源见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

## 插件简介

| 插件 | 添加目的与功能 |
| --- | --- |
| Reader（dsh-better-display） | 让长回复更易读：整理正文、推理、工具过程和生成文件。 |
| 进度播报（dsh-progress-narrator） | 减少等待时的不确定感：显示当前阶段、进度和简短状态。 |
| ACP（dsh-acp-official） | 延长有效对话：压缩上下文，并提供压缩层级与状态。 |
| 持久记忆（dsh-memory-official） | 跨会话保存可复用信息：记录、检索和审核安装者自己的记忆。 |
| 输出检查（dsh-output-watchdog） | 改善文件交付：检查生成文件与回复里的文件链接。 |
| 会话管理（dsh-session-manager） | 方便整理历史：提供会话列表、标注及回收站管理。 |
| Argo（argo-dsh） | 扩展研究能力：提供搜索、抓取与研究工具，含深度门控修复。 |
| 上下文面板（dsh-context） | 看清输入占用：显示上下文与工具定义的使用情况。 |
| 费用统计（dsh-cost-meter） | 了解调用成本：展示 token 用量和费用信息。 |
| 侧边栏（dsh-better-sidebar） | 便于切换工作内容：增强侧边栏、标题栏和工具入口。 |
| 基础面板（dsh-basics-panel） | 集中常用设置：提供基础操作与配置入口。 |
| 推理强度（dsh-reasoning-effort） | 在对话输入区快捷选择当前模型的推理强度。 |
| 模型能力与档位（dsh-thinking-effort-onetree） | 配置模型档位与网关值映射、子代理默认档位，并按提供商批量开关识图。 |
| 插件市场（dsh-community-market） | 方便发现扩展：查询和管理社区插件来源。 |
| 重写（dsh-easyrewrite） | 方便修改消息：提供重写与再次生成的操作。 |
| 提示词设置（dsh-prompt-custom） | 保留自定义入口：可添加自己的提示词，默认关闭且内容为空。 |
| Skill Manager（dsh-skill-manager） | 管理安装者自己的 Skills：只保留现有管理界面，不附带 Skill 内容。 |
| WSL（dsh-wsl-workspace） | 在需要时使用 Linux 工作环境：连接 WSL 工作区，默认未启用。 |
| Blender（dsh-blender-official） | 在需要时制作三维内容：连接 Blender 工具链，默认未启用。 |
| 代理设置（dsh-proxy-retained） | 在需要时配置网络代理：保留通用代理入口，默认未启用。 |
