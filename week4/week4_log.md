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
