# Qwen3.8-Flash-Next 技术报告解析

本目录收录 Qwen Team《On the Design of Qwen3.8-Next Architecture: Evaluation, Efficiency, and Training Stability》的原始报告及中文深度解析。

## 阅读入口

- [HTML 分析](https://aceee-1222.github.io/technical-report-notes/Qwen/Qwen3.8-Flash-Next/analysis/qwen3.8-flash-next-analysis.html)
- [PDF 分析](analysis/qwen3.8-flash-next-analysis.pdf)
- [页面总览](analysis/qwen3.8-flash-next-overview.png)
- [原始技术报告](original/Qwen3.8-Flash-Next-Tech-Report.pdf)
- [官方发布博客](https://qwen.ai/blog?id=qwen3.8-flash-next)
- [官方模型页面](https://huggingface.co/Qwen/Qwen3.8-Flash-Next)
- [官方代码与报告仓库](https://github.com/QwenLM/Qwen3.8-Flash-Next)

## 分析范围

报告按照原文论证顺序梳理以下内容：

- 125B / 6B active 语言主干、51B N-gram Embedding、4B MTP 与公开多模态模型的口径差异；
- 3× Gated DeltaNet + 1× Qwen Sparse Attention 的 48 层混合 token-mixing 架构；
- QSA 的 micro-block indexer、两阶段 continued pretraining 与百万 token kernel 效率；
- 四分支 Gated Residual 的逐通道读门、标量写门、跨层路径和 FP8 residual state；
- N-gram Embedding 的 Layer 2 放置、host-memory prefetch 与条件记忆路线；
- Muon 参数分类、fused matrix 语义切分、Canzona 分布式执行和 CUDA Graph；
- batch size、learning rate、稳定性压力测试、训练与部署披露边界；
- GDN、DSA、AltUp、HC / mHC、GatedNorm、AttnRes、Engram 与 Muon 等技术谱系。

HTML 中引用的原报告插图位于仓库根目录的 `assets/qwen3.8-flash-next/`。
