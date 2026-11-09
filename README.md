# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.4.9`（普通版 Latest）
- 平台：Windows x64
- 形式：NSIS 安装程序
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

> v0.4.9 新增换机备份与恢复。空白设备可完整恢复业务数据和设置，已有数据的设备可选择增量或覆盖导入。数据库保持 v12。抖音请求兼容性和诊断提示有所改进，真实 403 仍待定位。

## AIagent 独立版

- 版本：`v0.4.1-AIagent`（Prerelease，不会替代普通版 Latest）
- 产品：`项目舆情与运营支持工具 AIagent版`
- 安装包：`GameSentimentTool-AIagent-v0.4.1-win-x64-Setup.exe`
- 下载：[前往 AIagent Prerelease](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/tag/v0.4.1-AIagent)

AIagent 版包含 AI 驾驶舱、作者资产与采买推荐、B站热度监测、设置分页和跨页面持续运行的周报 AI 任务，并与普通版使用不同的程序名、快捷方式、安装记录、userData 和在线更新频道。两版可以并行安装，但共享本地 `8765/32123` 端口，因此不能同时运行。AIagent 版只读取 `channels/agentver/latest.json`，不会回退到普通版 Latest；普通版仍只使用原有 `latest.json`。

AIagent v0.4.1 安装包 SHA-256：

```text
0D304724EF165911D4F8FE0D312DDBE21CF76C9FBDF672615D1C7D73BCB7A601
```

## 使用方式

1. 在最新 Release 页面下载 `GameSentimentTool-v0.4.9-win-x64-Setup.exe`。
2. v0.3.3 至 v0.4.8 用户可通过软件内更新获取 v0.4.9。本次未执行真实安装或升级测试。**v0.3.2 及更早版本必须手工下载 v0.4.9，并以管理员身份运行一次。** 旧版更新助手会在新的安装握手代码生效前自行退出，无法通过远端资源反向修复。
3. 安装程序检测到旧版本时会自动沿用原安装路径，全新安装使用默认目录。
4. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
A6435BFE763E0C8316CFBBC0069000D91647A72DC7CE53D9EB84DA88A09BBBB3
```

## 发布验证约定

默认执行源码测试、构建、安装包内容、版本、大小、SHA-256、更新清单及远端资产元数据校验。资产回下载、运行冒烟、真实下载安装和覆盖升级测试仅在用户明确要求时执行；本次未执行这些实机验收。历史版本的真实升级记录不代表本版本已经实测。

## 更新检查

普通版内置本仓库地址，通过 `latest.json` 严格校验版本、固定下载地址、大小和 SHA-256 后才允许安装。AIagent 版通过 `channels/agentver/latest.json` 使用独立清单，并额外严格校验 `channel: "agentver"`、`-AIagent` 标签及专属安装包名称。v0.3.3 起，应用先请求管理员权限并确认 NSIS 已启动，再退出旧客户端；取消 UAC 或安装助手未就绪时客户端保持运行。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。

开发者：安索Anso。
