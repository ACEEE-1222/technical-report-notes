# openPangu 2.0 技术报告解析

本目录收录 Huawei / openPangu Team《openPangu-2.0: Towards Reliable and Efficient Agentic Reasoning》的原始报告及中文深度解析。

## 阅读入口

- [HTML 分析](https://aceee-1222.github.io/technical-report-notes/Huawei/openPangu-2.0/analysis/openpangu-2-analysis.html)
- [PDF 分析](analysis/openpangu-2-analysis.pdf)
- [原始技术报告](original/openPangu-2.0-Tech-Report.pdf)
- [官方模型页面](https://huggingface.co/openpangu/openPangu-2.0-Pro)
- [官方推理仓库](https://gitcode.com/ascend-tribe/openPangu-2.0-Infer)

## 分析范围

报告按照原文脉络梳理以下内容：

- openPangu-2.0-Flash、Pro 与 30B / 2B active 端侧模型的定位和配置；
- MLA、Hybrid DSA–SWA、PAS、ModAttn、MoE、mHC、MTP 与 Muon 等架构和训练设计；
- 34.4T token 预训练课程、Tokenizer、四类 RL 专家、多教师 OPD 与训练—推理一致性；
- Felix CP、W8A8、融合算子、Omni Cache、异步调度和 LoPT 等昇腾系统优化；
- 性能数字的适用口径，以及各项设计的技术谱系与证据等级。

HTML 中引用的原报告插图位于仓库根目录的 `assets/openpangu-2/`。
