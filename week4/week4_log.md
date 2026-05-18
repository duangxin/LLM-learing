# Week 4 学习记录（5.12 - 5.18）

## 文献阅读

### 6. Align Before Fuse: Vision and Language Representation Learning with Momentum Distillation
**ALBEF** | Li et al., 2021 | 【略读】

**阅读重点**
- 图文对齐与深度融合之间的过渡性工作，提出"先对齐再融合"的思想，并引入 momentum distillation
- 不属于最终形态，但能很好展示早期视觉语言预训练如何在对齐与融合之间寻找平衡
- 适合作为理解 BLIP 系列演进逻辑的背景

**笔记**

---

### 7. BLIP: Bootstrapping Language-Image Pre-training for Unified Vision-Language Understanding and Generation
**BLIP** | Li et al., 2022 | 【略读】

**阅读重点**
- 视觉语言统一建模的重要过渡工作，核心贡献是通过 bootstrapping 方式清洗和增强图文数据
- BLIP 属于"纯视觉语言预训练"时代，和后续"接入 LLM"的 MLLM 范式有跳跃，精读价值相对有限
- 重点把握 bootstrapping 数据清洗的思路与动机

**笔记**

---

### 8. BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models
**BLIP-2** | Li et al., 2023 | 【精读】

**阅读重点**
- 连接传统视觉语言预训练与现代 MLLM 的重要桥梁
- 提出 Q-Former 作为轻量级连接模块，在冻结视觉编码器和冻结 LLM 的前提下实现高效多模态对齐
- 重点理解：Q-Former 的设计、两阶段训练方式、冻结大模型带来的成本与性能权衡

**笔记**

---

### 9. Flamingo: a Visual Language Model for Few-Shot Learning
**Flamingo** | Alayrac et al., 2022 | 【略读】

**阅读重点**
- 首次证明 few-shot 多模态 in-context learning 可行
- 核心思想是将冻结的视觉编码器与冻结的 LLM 通过跨注意力机制连接
- 由于工程细节和训练成本较高，重点把握其历史定位和"如何把视觉信息高效注入 LLM"的思想
- 与 BLIP-2、LLaVA 形成对照

**笔记**

---

## 知识学习

### 蒸馏（Distillation）
- 蒸馏是一种模型压缩技术，旨在将一个大型、复杂的教师模型（Teacher Model）中的知识转移到一个较小、较简单的学生模型（Student Model）中。通过让学生模型模仿教师模型的输出，可以在保持性能的同时减少模型的参数量和计算资源需求。

### 多模态对齐
- 多模态对齐是指在多模态学习中，将来自不同模态（如图像、文本、音频等）的数据映射到一个共享的表示空间中，使得它们之间的关系能够被模型理解和利用。对齐的目标是让模型能够捕捉不同模态之间的语义关联，从而实现更有效的多模态理解和生成。
- 分为全局对齐和局部对齐。将整张图片和整段文本看作一个整体进行对齐；将图像中的特定区域（Region/Patch）与文本中的特定词（Token）建立对应关系。
