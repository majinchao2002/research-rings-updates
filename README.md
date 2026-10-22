# Research Rings 更新分发

此仓库分发 Research Rings 的 macOS 安装包与 Sparkle 订阅，以及 Zotero 插件 XPI、SHA-256 和原生更新清单；两个源码仓库继续私有。

Research Rings 提供论文阅读篇数、科研时间和 Workflow 优化时间三个每日目标圆环，可独立使用，也可连接 Zotero 阅读状态。

## 安装与更新

当前版本：**1.17.2（构建 8）**。

[下载 Research Rings for macOS](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/Research-Rings-1.17.2-8.zip) · [SHA-256 校验和](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/Research-Rings-1.17.2-8.zip.sha256)

**已经安装：优先使用「更多 → 检查更新…」或设置页的检查更新。** 下载、签名验证、替换与重启由 App 完成，数据保存在原容器中。当前手动检查，不在后台自动安装。

首次安装或更新故障回退才下载 ZIP，解压后将 `Research Rings.app` 放入「应用程序」，只保留一个正式 App。

当前支持搜索 Zotero 论文直接开始阅读；本机 Zotero 设为 `/inreading` 也会开始计时，Ring 选择论文会回写在读，`/read` 自动结束该篇、关联耗时并更新圆环。双向操作需要插件 0.3.0 和 Zotero 运行，过期或远端操作不自动启动本机计时。先点击活动类型，再选择对应项目或 Zotero 论文；科研只显示科研标签，Workflow 只显示开发标签。当前活动支持同类别切换，确认前计时保持，返回不打断。手动填写名称时不可为空。科研与 Workflow 可选择外部导入的项目标签，App 只保存名称，不读取 Obsidian 笔记。渐变圆环、逐篇用时、平均值与最近 20 篇趋势继续保留。

本机已通过内置更新完成 1.15 → 1.16 → 1.17 → 1.17.1，原有记录、目标、配置与 Zotero 文件夹授权保留；已验证双向计时、暂停不累计、回传去重和标签计时。临时论文已回收，测试计时及自动生成的未引用候选已清理。第二台实体 Mac 仍待验收。

- 系统要求：macOS 14 或更高，Apple Silicon / Intel。
- 更新订阅：`https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/appcast.xml`
- 更新包使用 Sparkle Ed25519 签名，App 内置公钥验证。
- 暂未使用 Apple Developer ID 公证，首次安装可能需要 macOS 手动确认；这与更新包签名是两回事。
- 本仓库不包含用户数据库、论文记录、同步文件夹或签名私钥。

发布由维护者确认验证结果后进行，不直接将每次开发构建推给使用者。

## Zotero 插件

当前版本：**0.3.0**，要求 **Zotero 10**（本机实测 10.0.6）。不需要 GitHub 登录、付费账号、MCP 或额外更新器。

[下载 Zotero 插件](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/zotero/research-rings-zotero-0.3.0.xpi) · [SHA-256 校验和](https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/zotero/research-rings-zotero-0.3.0.xpi.sha256)

首次安装：Zotero「工具 → 插件 → 右上角齿轮 → Install Plugin From File…」，选择 XPI。点 Research Rings 插件名称进入详情，将 **Allow automatic updates → On**。此后由 Zotero 定期检查并安装新版；插件更新与 Mac App 更新独立。

**0.2.0 及以前的迁移**：旧版更新地址指向私有仓库，不能自行发现公开新版。覆盖安装一次当前新版，保持同一插件 ID 即可保留配置和历史，不要卸载或删除数据。新设备也先安装本页 XPI，再选择已有联动文件夹。

已在本机经 Zotero 原生更新到 0.3.0，自动更新继续 On，原文件夹配置保留；重启 Zotero 后完成双向在读、回写标签、已读结束与普通标签保留的实测。第二台实体 Mac 尚待验收。

- 更新清单：`https://raw.githubusercontent.com/majinchao2002/research-rings-updates/main/zotero/update.json`
- XPI 使用 HTTPS 下载，由 Zotero 按清单中的 SHA-256 验证；与 Mac App 的 Sparkle Ed25519 签名分开。
- 公开包仅含 manifest、bootstrap 和桥接运行代码，不含论文、笔记、用户配置或凭据。XPI 中的 JavaScript 可被查看，私有源码仓库并不使已分发运行代码保密。
- 已发布版本不可替换内容；修复时提升版本，发布新包与更新清单。
