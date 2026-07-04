# 小盾龙 Portrait Clearance 下载

本仓库（`QAyong/xiaodunlong-releases`）仅用于发布小盾龙 Portrait Clearance 的可分发安装包、校验文件和极简使用说明。

源码仓库、完整 Skill 文档、内部 references、测试数据和工程文档不在本仓库公开。

## 当前状态

- 仓库已创建并初始化（`main` 分支含 README）
- 已发布占位 release `v0.1.0-placeholder`，用于打通 `/releases/latest` 链路
- 本地已生成 `distribution/latest.json` manifest 草稿和 release 产物校验信息
- 公开 release 仍需上传 `latest.json` manifest 与正式安装包，`.../latest/download/latest.json` 链接在上传附件后才会生效
- 源码仓库：`https://github.com/QAyong/portrait-clearance`（私有）

## 下载

最新版本信息：

```text
https://github.com/QAyong/xiaodunlong-releases/releases/latest/download/latest.json
```

每次下载后都应校验 SHA256。不要安装校验失败的文件。

## Windows

下载 `小盾龙短剧合规平台-Lite-安装包.exe`，校验 SHA256 后运行安装。

安装完成后，打开新终端验证：

```powershell
portrait-clearance --help
portrait-clearance resources model status
```

## macOS

下载 `小盾龙短剧合规平台-macOS-preview.zip`，校验 SHA256 后解压，将 `.app` 移动到 `/Applications`。

当前 macOS 包是技术预览版，未签名和 notarization，首次打开可能需要在系统设置中允许。

## 给 AI 的安装指令

可以把下面这段复制给 ChatGPT / Claude / Codex / Cursor：

```text
请帮我安装“小盾龙短剧合规平台”。

请先判断我的操作系统，然后从官方 manifest 获取最新下载信息：
https://github.com/QAyong/xiaodunlong-releases/releases/latest/download/latest.json

请优先使用 direct_url 下载；如果 GitHub 下载失败或速度过慢，再询问我是否使用 mirror_urls 中的 GitHub 镜像源。
下载完成后必须校验 SHA256，校验通过后再安装。

Windows：使用 install_args 静默安装，安装后验证 portrait-clearance --help。
macOS：下载 zip 后校验、解压，将 app 移动到 /Applications，并提醒我当前为未签名技术预览版。
```

## CLI / Agent 使用

极简 CLI 使用说明见：

```text
AGENT_USAGE.md
```

请使用审慎表述。报告结果不是司法鉴定、律师意见或法院结论。
