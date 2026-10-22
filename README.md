# Research Rings 更新分发

此仓库只分发 Research Rings 的 macOS 安装包、版本说明和 Sparkle 更新订阅；源码在独立私有仓库维护。

Research Rings 提供论文阅读篇数、科研时间和 Workflow 优化时间三个每日目标圆环，可独立使用，也可连接 Zotero 阅读状态。

## 安装与更新

首个正式更新包准备中。安装带更新功能的版本后，可通过菜单栏「更多 → 检查更新…」或设置页检查并安装后续版本。安装更新替换同一个 App，科研数据保存在原有本地容器中。

- 系统要求：macOS 14 或更高，Apple Silicon / Intel。
- 更新订阅：`https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/appcast.xml`
- 更新包使用 Sparkle Ed25519 签名，App 内置公钥验证。
- 暂未使用 Apple Developer ID 公证，首次安装可能需要 macOS 手动确认；这与更新包签名是两回事。
- 本仓库不包含用户数据库、论文记录、同步文件夹或签名私钥。

发布由维护者确认验证结果后进行，不直接将每次开发构建推给使用者。
