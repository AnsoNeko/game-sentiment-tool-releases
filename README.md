# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.2.4`
- 平台：Windows x64
- 形式：NSIS 安装程序
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

> 2026-07-14 兼容修订：v0.2.4 安装包已重新打包。初版 v0.2.4 会因 Windows 产品显示名变化而读取新的空 userData 目录，旧数据并未丢失。修订包恢复读取历史目录 `%APPDATA%\toolbox-sentiment-electron`。已经下载或安装初版 v0.2.4 的用户请从 Release 页面重新下载安装包并直接覆盖安装；同版本更新不会触发应用内版本提示。不要手工复制、合并或删除 userData 目录。

## 使用方式

1. 在最新 Release 页面下载 `GameSentimentTool-v0.2.4-win-x64-Setup.exe`。
2. 运行安装程序，可选择安装目录，并按需创建桌面和开始菜单快捷方式。
3. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
A6FEAD6864FD254771A7CB050C5A8EEF54B2EC9043EC94A0A82BEAA76CADC588
```

## 更新检查

软件内置本仓库地址，优先通过 GitHub 公开 Release 网页跳转检查版本，并在必要时使用 API 回退。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。

开发者：安索Anso。
