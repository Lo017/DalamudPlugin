# Lo017 的 Dalamud 插件库

Lo017 维护的 Dalamud 第三方插件库。

## 安装

将以下地址添加到 Dalamud 设置中的自定义插件仓库列表：

```text
https://raw.githubusercontent.com/Lo017/DalamudPlugin/main/repo.json
```

1. 在自定义插件仓库列表中粘贴上述地址，添加并启用该项，然后保存设置。
2. 打开插件安装器，等待插件列表刷新。
3. 搜索所需插件，点击安装。

插件发布后会显示在插件安装器中；已安装插件的新版通过插件安装器更新。

## 插件

| 插件 | 功能 | 源码 |
| --- | --- | --- |
| 挖宝账本 TreasureLedger | 国服挖宝记录、工资结算、宝图位置和提醒 | [Lo017/TreasureLedger](https://github.com/Lo017/TreasureLedger) |

## 收录与更新

[repo.json](repo.json) 保存本库的插件列表。每个插件占一个条目，包含插件名称、内部名称、作者、版本号、Dalamud API 级别、功能描述、源码仓库地址，以及安装和更新所用的 ZIP 下载链接。

安装包存放在本仓库的 `plugins/<插件内部名称>/<版本号>/latest.zip`，例如 `plugins/TreasureLedger/0.6.1.0/latest.zip`。安装包包含插件 DLL、插件清单及运行所需的依赖文件。

上传安装包后，将对应的 `raw.githubusercontent.com` 下载地址填入 `repo.json` 的安装与更新链接。源码仓库地址填写在 `RepoUrl` 中。

发布新版时，同步更新 `AssemblyVersion`、`DownloadLinkInstall`、`DownloadLinkUpdate`、`DownloadLinkTesting` 和 `LastUpdate`；`DalamudApiLevel` 与该安装包实际使用的 API 级别保持一致。

库清单采用 [Dalamud 自定义插件库格式](https://dalamud.dev/plugin-publishing/custom-repositories/)。
