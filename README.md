# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.3.1`
- 平台：Windows x64
- 形式：NSIS 安装程序
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

> v0.3.1 新增反链数据采集与作者库，支持 B站、抖音、小红书主页按关键词和日期范围查找作品及公开互动指标；同时取消评论采集 300 条硬上限，超过 300 条仅显示风险提示。

## 使用方式

1. 在最新 Release 页面下载 `GameSentimentTool-v0.3.1-win-x64-Setup.exe`。
2. 运行安装程序；检测到旧版本时会自动沿用原安装路径，全新安装使用默认目录。
3. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
EB7D999F65AF96D8C83CDF96419A399E59C13C9C0C1613B8FDEA0F38CFFCCB23
```

## 更新检查

软件内置本仓库地址，优先通过 GitHub 公开 Release 网页跳转检查版本，并在必要时使用 API 回退。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。

开发者：安索Anso。
