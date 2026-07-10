# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.2.1`
- 平台：Windows x64
- 形式：NSIS 安装程序
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

## 使用方式

1. 在最新 Release 页面下载 `GameSentimentTool-v0.2.1-win-x64-Setup.exe`。
2. 运行安装程序，可选择安装目录，并按需创建桌面和开始菜单快捷方式。
3. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
8A0E76B7E7318CB2AA678A7E17947C2EC210F99963EF55901F1E69FCD64BCD4D
```

## 更新检查

软件内置本仓库地址，通过 GitHub 公开 `releases/latest` 接口检查版本。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。
