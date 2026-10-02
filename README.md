# 一树 · DSH Desktop 配置分享包

非官方个人配置组合包，针对 **DeepSeek Harness Desktop 0.2.0-rc.2**。把阅读界面、ACP 压缩、研究工具和工作习惯组合成一个可安装插件。它不会提供模型账户；安装者使用自己的模型配置。

## 下载与安装

1. 从 [v0.1.0 Release](https://github.com/S-AN-Shu/dsh-onetree-desktop-pack/releases/tag/v0.1.0) 下载 `dsh-onetree-desktop-pack-0.1.0.zip`，解压。
2. 打开 Desktop 左侧 **插件 → 添加插件**，输入解压后的 `dsh-onetree-desktop-pack-0.1.0.tgz` 的本地绝对路径。
3. 完成安装后选择 **立即启用**。在新会话的预设选择器里选择 **一树 · 标准 / PTC / 精简 / Cordis**。

也可以在「添加插件」直接粘贴下面的压缩包地址，免去下载 ZIP：

```text
https://github.com/S-AN-Shu/dsh-onetree-desktop-pack/releases/download/v0.1.0/dsh-onetree-desktop-pack-0.1.0.tgz
```

ZIP 是下载集合；**实际安装格式为 `.tgz`，不要把 ZIP 当插件导入，也不要覆盖自己的 `.dsh` 目录**。安装需要联网下载组件及公共 npm 依赖。ZIP 中组件归档供检查与留存，不是完整离线安装器。不要分别启用组件再启用本组合包，否则可能重复加载。

## 内容

- Reader 阅读界面、进度旁白、侧边栏、基础面板、上下文与费用显示、推理强度、社区插件市场、重写功能及 Skill 管理插件的通用代码。
- ACP 与四个新 ID 预设：`onetree-standard`、`onetree-ptc`、`onetree-minimal`、`onetree-cordis`。保留接收者原有预设；不修改其默认模型或默认预设。
- Argo 原生研究工具代码，包含子代理深度门控和失败摘要修复；ACP 层级显示修复也来自维护后的副本。
- 深色主题、忙碌时 Enter 排队、详细性能显示、侧边栏设置；基础面板关闭直接删除会话。
- 一树协作规则：保留工作方式，移除个人 Wiki、Skill 路径及本机基础设施要求。

组件和版本见 [CONTENTS.json](CONTENTS.json)。主包按官方 `dsh.bundle.patch` 合同按顺序加载组件配置层，再应用可共享偏好。

## 接收者需要自行配置的部分

- **模型**：使用 Desktop 自己的账户/提供商设置。本包不包含 API Key、登录状态、个人接口地址或模型参数。
- **Argo**：搜索/抓取仍需要它的公共后端及外部 Node/npm（`npx`）、Python 3.9+ / PyYAML。Desktop 内置 Node 不等于系统已经有 `npx`。本包不安装这些系统依赖，也没有包含原维护机器的搜索命令或引擎目录。
- **Blender、代理、WSL**：通用代码归档随包提供，默认禁用。没有预设会自动启动这些外部服务。需要时请配置自己的程序及工作目录后再启用。
- **记忆及个人集成**：整个组件不随包分发。记忆归档含角色样本、生成报告和知识词表，无法把它作为纯配置公开。便携预设已移除这些接入；接收者如需记忆可自行安装、配置自己的空存储。此分享包共 18 个组件。
- **Skills**：没有任何 Skill 文件或 Skill 目录。通用 Skill 管理界面代码与私人 Skill 内容是两回事；便携预设不注入个人 Skills。

现有 profile/home 的用户补丁优先于组合包，可能覆盖其偏好。卸载或禁用主组合包可撤回它贡献的配置层；接收者现有用户补丁及数据按宿主管理。

## 隐私与验证

发布内容由文件白名单生成，未复制个人 profile、node_modules 整体、锁文件或 home。排除所有 Skills、Wiki、会话、聊天导出、记忆图谱、数据库、账户、凭据、私人路径、日志、备份及旧 web profile。组件自带的 Skills 目录同样移除。

验证结果会随 Release 的 `VALIDATION.json` 提供，包括归档递归检查、官方组合解析、隔离安装及发布下载哈希复核。未通过接收者的真实 Desktop GUI、模型请求或外部服务链路验证；请按自己的环境完成首次使用配置。兼容范围固定为上述 runtime 版本，升级后需要重新验证。

## 许可与来源

配置及协作规则采用 MIT；各组件保持各自的 MIT、BSD-3-Clause、Apache-2.0 等原许可与现存版权声明，见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) 及组件内部许可证。`.share.1` 版本表示为此发布进行过隐私整理的维护副本，不是上游官方发布版本。

官方合同参考：[打包与安装插件](https://github.com/deepseek-ai/deepseek-harness/blob/master/docs/user/develop/basic/publish.zh.md)、[Desktop 插件管理界面](https://github.com/deepseek-ai/deepseek-harness/blob/master/packages/client/ui-plugin-manager/README.zh.md)、[配置层与解析](https://github.com/deepseek-ai/deepseek-harness/blob/master/packages/boot/app-boot/README.zh.md)。
