# 项目舆情与运营支持工具

这是“项目舆情与运营支持工具”的公开更新与发行仓库，仅用于发布版本说明和 Windows Release 安装包，不包含项目源码、业务数据库或用户配置。

## 最新版本

- 版本：`v0.2.0`
- 平台：Windows x64
- 形式：Portable EXE，无需安装
- 下载：[前往最新 Release](https://github.com/AnsoNeko/game-sentiment-tool-releases/releases/latest)

## 使用方式

1. 在最新 Release 页面下载 `项目舆情与运营支持工具 0.2.0.exe`。
2. 将 EXE 放在希望长期保存的位置后直接运行。
3. 软件的项目、评论、Cookie、安全配置和 AI 配置均保存在当前 Windows 用户的本地应用数据目录中，不会存入本仓库。

当前版本未进行代码签名，Windows SmartScreen 可能显示未知发布者提示。请只从本仓库的 Release 页面下载，并可使用下列 SHA-256 校验文件：

```text
76735AB54B1D4A1BB0E3114E8B7BB0E8576FC54EA3AD0EC0312F64222F8D29FE
```

## 更新检查

软件内置本仓库地址，通过 GitHub 公开 `releases/latest` 接口检查版本。检查更新不会上传本地项目数据、玩家评论、Cookie、API Key、Prompt 或安全设置。

版本变化请查看 [CHANGELOG.md](CHANGELOG.md)。
