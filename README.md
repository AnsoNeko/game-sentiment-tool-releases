# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.4.11`（普通版 Latest）
- 平台：Windows x64
- 形式：NSIS 安装程序
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

> v0.4.11 优化舆情池批量清理。确认后显示实际处理条数和提交状态，成功后自动刷新舆情池。数据库保持 v12。

## AIagent 独立版

- 版本：`v0.4.9-AIagent`（独立 Prerelease）
- 产品：`项目舆情与运营支持工具 AIagent版`
- 安装包：`GameSentimentTool-AIagent-v0.4.9-win-x64-Setup.exe`
- 下载：[前往 AIagent Prerelease](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/tag/v0.4.9-AIagent)

AIagent 已同步普通版 v0.4.9 的业务功能。驾驶舱按当前任务选择工具、定向查询项目和报告，并减少业务列表刷新。换机备份仅迁移业务数据，保留本机驾驶舱历史。

AIagent 使用独立的程序名、快捷方式、安装记录、userData 和更新频道，只读取 `channels/agentver/latest.json`。两版可以并行安装，共享的本地 `8765/32123` 端口限制两版同时运行。

AIagent v0.4.9 安装包 SHA-256：

```text
5131F12917F4BE7283408A77C3AECDB56786F8CA9FB04BC6DFDC23E7F496DC0A
```

## 使用方式

1. 在最新 Release 页面下载 `GameSentimentTool-v0.4.11-win-x64-Setup.exe`。
2. v0.3.3 至 v0.4.10 用户可通过软件内更新获取 v0.4.11。本次未执行真实安装或升级测试。**v0.3.2 及更早版本必须手工下载 v0.4.11，并以管理员身份运行一次。** 旧版更新助手会在新的安装握手代码生效前自行退出，无法通过远端资源反向修复。
3. 安装程序检测到旧版本时会自动沿用原安装路径，全新安装使用默认目录。
4. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
F83BEC331B9308F36051E4F55BB18B9315D7EA89392547815FD4CFDBFB8ED7E5
```

## 发布验证约定

默认执行源码测试、构建、安装包内容、版本、大小、SHA-256、更新清单及远端资产元数据校验。资产回下载、运行冒烟、真实下载安装和覆盖升级测试仅在用户明确要求时执行；本次未执行这些实机验收。历史版本的真实升级记录不代表本版本已经实测。

## 更新检查

普通版内置本仓库地址，通过 `latest.json` 严格校验版本、固定下载地址、大小和 SHA-256 后才允许安装。AIagent 版通过 `channels/agentver/latest.json` 使用独立清单，并额外严格校验 `channel: "agentver"`、`-AIagent` 标签及专属安装包名称。v0.3.3 起，应用先请求管理员权限并确认 NSIS 已启动，再退出旧客户端；取消 UAC 或安装助手未就绪时客户端保持运行。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。

开发者：安索Anso。
