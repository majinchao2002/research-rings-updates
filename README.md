# Research Rings 更新分发

此仓库只分发 Research Rings 的 macOS 安装包、版本说明和 Sparkle 更新订阅；源码在独立私有仓库维护。

Research Rings 提供论文阅读篇数、科研时间和 Workflow 优化时间三个每日目标圆环，可独立使用，也可连接 Zotero 阅读状态。

## 安装与更新

当前版本：**1.15.0（构建 4）**。

[下载 Research Rings for macOS](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/Research-Rings-1.15.0-4.zip) · [SHA-256 校验和](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/Research-Rings-1.15.0-4.zip.sha256)

解压后将 `Research Rings.app` 放入「应用程序」，替换旧版即可。之后可通过「更多 → 检查更新…」或设置页下载、验证并安装后续版本。安装更新替换同一个 App，科研数据保存在原有本地容器中。当前仅手动检查，不自动在后台安装。

1.15.0 新增 Fitness 风格渐变圆环，阅读篇数与用时同一行显示；提供逐篇累计用时、平均耗时与最近 20 篇变化。没有计时的论文单独标明，不计入平均值；可跨天继续阅读，也可明确关联 Zotero 已读记录的计时。多 Mac 使用论文关联时需都升级到 1.15.0 或更高。

本机已通过内置更新从 1.14.0（构建 3）升级到 1.15.0（构建 4）并重启，科研记录、论文完成、每日目标、设置和 Zotero 文件夹授权保留。取消与 Esc 返回今日圆环的修复继续保留。

- 系统要求：macOS 14 或更高，Apple Silicon / Intel。
- 更新订阅：`https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/appcast.xml`
- 更新包使用 Sparkle Ed25519 签名，App 内置公钥验证。
- 暂未使用 Apple Developer ID 公证，首次安装可能需要 macOS 手动确认；这与更新包签名是两回事。
- 本仓库不包含用户数据库、论文记录、同步文件夹或签名私钥。

发布由维护者确认验证结果后进行，不直接将每次开发构建推给使用者。
