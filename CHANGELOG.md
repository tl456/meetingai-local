# Changelog

## v2.0.2

- ASR 语义标注可视化：语义校验状态、AI辅助/原始逐字稿切换、待确认入口与详情。
- `corrected / uncertain / critical_uncertain` 轻量标记。
- 历史会议支持重新执行语义校验。
- 音频导入任务展示语义校验状态。
- 原始 `transcript.jsonl` 仍为不可变证据；语义结果写入独立 sidecar。

## v2.0.1

- 增加 ASR Semantic Annotation sidecar。
- 支持保守 / 均衡 / 积极强度与关键事实阈值。
- AI 标注失败自动回退原始逐字稿。

## v2.0.0

- 增加 MP3 等超长音频导入。
- 增加 CPU / GPU / CUDA / FFmpeg / 依赖运行环境检测。
- 增加 ASR 模型推荐和切换。
- 增加中国大陆 Pip / 模型镜像以及按作用域代理。
