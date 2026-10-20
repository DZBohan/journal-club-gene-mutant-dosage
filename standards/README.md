# Journal club 可复用标准

版本：1.0，2026-10-20。适用于新文章，不局限于 INCOMMON 或 SelectSim。

## 快速使用

把文章 PDF 交给执行者，并使用以下指令：

> 按本仓库 standards/ 的 journal club 标准处理这篇文章。先核查正文、Methods、图注与相关补充材料，建立证据表；制作中文文献解读 HTML 和英文 journal club PPTX，附英文演讲备注与 PDF 预览。默认报告约 20 分钟，使用原文 figure panels 加自绘方法示意图。区分工具核心方法、数据集应用、下游模型和我们提出的实验。交付前完成科学内容与逐页视觉检查。缺失材料、未验证项和需要我决定的问题请明确指出。

该指令同时请求两种交付；若用户只要求解读、PPT 或修改单页，则只执行对应范围，不自动扩展任务。

## 阅读顺序

1. [流程与证据标准](workflow.md)：从接收文章到讨论、修订和归档。
2. [文献解读 HTML 标准](reading-html.md)：完整解释，而非摘要翻译。
3. [PPT 标准](presentation.md)：服务现场讲解，不把 HTML 压缩贴满页面。
4. [验收清单](acceptance.md)：发布前逐项填写，不把未完成项标为通过。
5. [任务模板](../templates/journal-club/brief.md)、[证据表](../templates/journal-club/evidence.csv)、[图版登记表](../templates/journal-club/panels.csv)、[逐页脚本](../templates/journal-club/slide-plan.csv)、[验收记录](../templates/journal-club/review.md)。

## 默认交付与边界

- 文献解读：中文、单文件离线 HTML。英文版按要求增加，两版证据、数字与限定条件一致。
- 演示：英文、约 20 分钟；页数由逻辑决定，不强制 20 页。必须直接交付可编辑 PPTX，附 PDF 预览与备注。
- 研究对象、数据和结论以该文为准。不把旧文章参数、颜色含义、结论或实验建议机械移植。
- 当前任务的明确要求优先于默认值。偏离标准要在任务记录说明原因。
- 本标准位于既有唯一仓库，不重建重复仓库；旧 INCOMMON 文件保留原位。新文章若存入本仓库，使用 `papers/<year-short-title>/` 独立目录，不混入既有 approved slides。只在获授权时归档文章材料。
- `draft`、`reviewed`、`approved` 分开：检查完成不等于用户批准。原始 PDF 与原文图片公开提交前检查许可和授权；默认只存来源、引用和允许共享的派生成品，不顺手上传整篇 PDF。

## 设计原则

准确优先；每一步都能说明输入、操作、输出、目的。保留关键方法，减少重复说明。统计发现不是机制证明，内部验证不是外部临床验证。用户看不懂时修正表达或图示，而不是仅在聊天里补救。
