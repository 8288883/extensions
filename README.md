# Komikku 商店根清单兼容修复

本修复包用于解决将资源迁移到 `store/` 二级目录后，Komikku 无法读取商店或仍使用旧清单路径的问题。

## 包含文件

| 文件 | 上传位置 | 作用 |
|---|---|---|
| `index.json` | 仓库根目录 | 商店索引；恢复指向根 `extensions.json`。 |
| `extensions.json` | 仓库根目录 | 14 个扩展的兼容清单；APK 与 logo 链接仍全部指向 `store/`。 |
| `README.md` | 仓库根目录，可选 | 更新后的目录和刷新说明。 |

`store/` 文件夹不在本修复包中。它已经在仓库中，且其中的 14 项扩展清单、28 条当前 APK/logo Raw 资源链接均已在线返回 HTTP 200。

## 手机操作

在 GitHub 仓库根目录直接替换本包内的 `index.json` 和 `extensions.json`；`README.md` 可一并替换。不要删除 `store/` 文件夹，也无需再次上传 APK。

提交后，在 Komikku 中删除现有的该商店条目，再重新添加：

```text
https://raw.githubusercontent.com/8288883/extensions/main/index.json
```

随后强制停止 Komikku，重新打开后刷新扩展商店。这样会清除应用继续使用旧 `extensionListUrl` 或旧根清单缓存的情况。

## 最终布局

```text
index.json
extensions.json
README.md
store/
  extensions.json
  tibiu/
  nyahentai/
  ...
```

根与 `store/` 下的两个 `extensions.json` 内容完全相同；根文件仅用于兼容读取入口，实际 APK 和 logo 均集中在 `store/` 下。
