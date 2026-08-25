# Komikku 扩展商店

本仓库为 Komikku v1.14.1 / TachiyomiX 1.6 扩展商店。商店索引地址为：

```text
https://raw.githubusercontent.com/8288883/extensions/main/index.json
```

## 目录结构

每个网站的当前发布资源均位于独立目录，便于分别维护版本、图标与后续更新。

| 目录 | 当前扩展 | 当前版本 | APK |
|---|---|---:|---|
| `tibiu/` | TIBIU 漫画 | `1.0.3` | `TIBIU-Komikku-v1.0.3-debug.apk` |
| `nyahentai/` | Nyahentai | `1.0.1` | `Nyahentai-Komikku-v1.0.1-debug.apk` |

`extensions.json` 只引用上述目录中的当前 APK 和图标。根目录的旧版 APK 与旧图标暂时保留，以免已缓存旧清单的客户端出现下载失败；在确认所有客户端完成刷新后，可以另行删除这些兼容文件。

## 更新扩展

在 Komikku 中刷新此商店后，安装对应的更高版本号即可更新。若客户端仍显示旧条目，请强制停止并重新打开 Komikku，然后刷新商店；必要时删除商店后重新添加上述索引地址。

这些扩展均标注为 **NSFW**，仅限已获授权的成年用户使用。
