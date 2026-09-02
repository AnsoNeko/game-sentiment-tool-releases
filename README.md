# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.4.1`
- 平台：Windows x64
- 形式：NSIS 安装程序
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

> v0.4.1 将系统通用设置拆分为 5 个业务分页，并让普通 AI 周报与历史变化报告在切换页面后继续接收进度和正文；全局任务条可从任意页面查看、停止并保留终态提示。

## AIagent 独立版

- 版本：`v0.3.4-AIagent`（Prerelease，不会替代普通版 Latest）
- 产品：`项目舆情与运营支持工具 AIagent版`
- 安装包：`GameSentimentTool-AIagent-v0.3.4-win-x64-Setup.exe`
- 下载：[前往 AIagent Prerelease](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/tag/v0.3.4-AIagent)

AIagent 版包含 AI 驾驶舱，并与普通版使用不同的程序名、快捷方式、安装记录、userData 和在线更新频道。两版可以并行安装，但共享本地 `8765/32123` 端口，因此不能同时运行。AIagent 版只读取 `channels/agentver/latest.json`，不会回退到普通版 Latest；普通版仍只使用原有 `latest.json`。

AIagent v0.3.4 安装包 SHA-256：

```text
84A145419C3E443DCD6EF5DDFC6CC95D03960B9EE1316E5C1FA70B1C7255CC72
```

## 使用方式

1. 在最新 Release 页面下载 `GameSentimentTool-v0.4.1-win-x64-Setup.exe`。
2. v0.3.3-v0.4.0 用户可使用软件内更新升级到 v0.4.1。**v0.3.2 及更早版本必须手工下载 v0.4.1，并以管理员身份运行一次。** 旧版更新助手会在新的安装握手代码生效前自行退出，无法通过远端资源反向修复。
3. 安装程序检测到旧版本时会自动沿用原安装路径，全新安装使用默认目录。
4. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
608DB4AC676CFE975DD292BC09F06310ED0B3DB38FB104AED1FBC239AF88C24C
```

## 更新检查

普通版内置本仓库地址，通过 `latest.json` 严格校验版本、固定下载地址、大小和 SHA-256 后才允许安装。AIagent 版通过 `channels/agentver/latest.json` 使用独立清单，并额外严格校验 `channel: "agentver"`、`-AIagent` 标签及专属安装包名称。v0.3.3 起，应用先请求管理员权限并确认 NSIS 已启动，再退出旧客户端；取消 UAC 或安装助手未就绪时客户端保持运行。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。

开发者：安索Anso。
