# Research Rings 更新分发

此仓库分发 Research Rings 的 macOS 安装包与 Sparkle 订阅，以及 Zotero 插件 XPI、SHA-256 和原生更新清单；两个源码仓库继续私有。

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

## Zotero 插件

当前版本：**0.2.2**，要求 **Zotero 10**（本机实测 10.0.6）。不需要 GitHub 登录、付费账号、MCP 或额外更新器。

[下载 Zotero 插件](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/zotero/research-rings-zotero-0.2.2.xpi) · [SHA-256 校验和](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/zotero/research-rings-zotero-0.2.2.xpi.sha256)

首次安装：Zotero「工具 → 插件 → 右上角齿轮 → Install Plugin From File…」，选择 XPI。点 Research Rings 插件名称进入详情，将 **Allow automatic updates → On**。此后由 Zotero 定期检查并安装新版；插件更新与 Mac App 更新独立。

**0.2.0 及以前的迁移**：旧版更新地址指向私有仓库，不能自行发现公开新版。覆盖安装一次 0.2.2，保持同一插件 ID 即可保留配置和历史，不要卸载或删除数据。新设备也先安装本页 XPI，再选择已有联动文件夹。

已在本机从 0.2.1 通过 Zotero 原生更新至 0.2.2，并确认自动更新 On、安装包校验一致、插件历史与文件夹连接保留。第二台实体 Mac 尚待验收。App 1.16 的论文选择功能仍在独立验收，不因插件发布而宣称已交付。

- 更新清单：`https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/zotero/update.json`
- XPI 使用 HTTPS 下载，由 Zotero 按清单中的 SHA-256 验证；与 Mac App 的 Sparkle Ed25519 签名分开。
- 公开包仅含 manifest、bootstrap 和桥接运行代码，不含论文、笔记、用户配置或凭据。XPI 中的 JavaScript 可被查看，私有源码仓库并不使已分发运行代码保密。
- 已发布版本不可替换内容；修复时提升版本，发布新包与更新清单。
