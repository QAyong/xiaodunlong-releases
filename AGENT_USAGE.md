# Portrait Clearance Agent Usage

这是面向 AI Agent / CLI 调用的极简公开说明，不包含完整 Skill 工作流、风险评分细则、提示词或内部 references。

本机可通过 `portrait-clearance` CLI 执行肖像权可识别性排查。

常用命令：

- 查看配置：`portrait-clearance config get`
- 保存配置：`portrait-clearance config save --provider doubao --api-key ...`
- 检测配置：`portrait-clearance config check`
- 查看本地人脸模型：`portrait-clearance resources model status`
- 使用 ModelScope 国内镜像下载本地人脸模型：`portrait-clearance resources model install`
- 两图比对：`portrait-clearance compare <query> --ref <reference>`
- 网络搜图完整排查：`portrait-clearance clearance <image> --max-images 60 --scrolls 10`
- 查看历史：`portrait-clearance history list --limit 10`

默认不生成 DOCX；如需 Word 报告，添加 `--export-docx`。

发布包不内置真实 API Key。用户 Key 应通过 GUI 或 `config save` 写入当前用户的 `%LOCALAPPDATA%\portrait-clearance\multimodal.json`。

输出应使用审慎措辞，不得表述为“确认侵权”“确认同一人”“绝对安全”。

安装包内也可能包含本文件副本，路径通常位于应用安装目录的 `_internal/AGENT_USAGE.md`。
