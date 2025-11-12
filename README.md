# Notes-For-LLM

大语言模型（LLM）学习笔记与代码实现

## 📚 项目简介

本项目是一个系统化的大语言模型学习资源库，包含从基础概念到实际实现的完整学习路径。项目涵盖了注意力机制、GPT模型实现、预训练、微调等核心主题，并提供大量实践代码和补充材料。

## 📖 目录结构

### 1. [llm-intro](llm-intro/) - 理解大语言模型
- 大语言模型的基础介绍
- Python环境设置指南
- LLM开发生命周期概述

### 2. [attention](attention/) - 编写注意力机制
- **主要章节代码**：注意力机制的实现
- **补充材料**：
  - 高效多头注意力的不同实现变体
  - PyTorch 缓冲区概念解释（用于因果注意力机制）

### 3. [data-engineering](data-engineering/) - 处理文本数据
- **主要章节代码**：文本数据处理和练习解决方案
- **额外材料**：
  - 字节对编码器（BPE）实现与基准测试
  - 嵌入层与全连接层等价性解释
  - 数据加载器直观解释
  - 从零实现 GPT-2 BPE 分词器

### 4. [gpt-model](gpt-model/) - 从零实现GPT模型生成文本
- **主要章节代码**：GPT模型的完整实现
- **补充材料**：
  - GPT模型性能分析
  - KV缓存实现（加速推理）
  - GPT到Llama 3.2的转换指南

### 5. [pretraining](pretraining/) - 在未标记数据上进行预训练
- **主要章节代码**：预训练实现
- **额外材料**：
  - 替代权重加载方法
  - Project Gutenberg数据集上的预训练
  - 学习率调度器和梯度裁剪
  - 超参数调优脚本
  - 交互式用户界面
  - GPT到Llama 3.2转换指南
  - 内存高效的权重加载
  - GPT-2 BPE分词器从零实现
  - PyTorch训练速度优化技巧
  - Qwen3 0.6B和30B-A3B（MoE）实现
  - Gemma 3 270M实现（含KV缓存）
  - 训练循环增强功能（Bells and Whistles）

### 6. [fine-tuning](fine-tuning/) - 微调相关

#### [Fine-Tuning-For-Follow-Instructions](fine-tuning/Fine-Tuning-For-Follow-Instructions/) - 指令跟随微调
- **主要章节代码**：指令跟随微调实现
- **额外材料**：
  - 指令数据集准备工具
  - 使用本地Llama 3和GPT-4 API的模型评估
  - 直接偏好优化（DPO）实现
  - 合成数据集生成与改进
  - 交互式用户界面

#### [Fine-Tuning-For-Classification](fine-tuning/Fine-Tuning-For-Classification/) - 分类任务微调
- **主要章节代码**：分类任务微调实现
- **额外材料**：
  - 额外实验（最后vs第一个token训练、扩展输入长度等）
  - IMDb电影评论情感分类数据集对比
  - 交互式用户界面

#### [LoRA](fine-tuning/LoRA/) - 参数高效微调
- **主要章节代码**：LoRA（Low-Rank Adaptation）实现

### 7. [pytorch](pytorch/) - PyTorch相关内容
- **主要章节代码**：PyTorch基础与实践
  - PyTorch基础语法（A.1-A.8）
  - GPU使用（A.9）
  - 多GPU分布式训练（DDP）
  - 练习解决方案
- **设置建议**：环境配置推荐
  - Python环境设置
  - 库安装指南
  - Docker环境（可选）
  - AWS SageMaker Notebook（可选）

## 🚀 快速开始

### 环境要求

- Python >= 3.10, <= 3.13
- PyTorch >= 2.2.2
- TensorFlow >= 2.16.2 (部分章节需要)
- JupyterLab >= 4.0

### 安装依赖

```bash
# 使用 pip 安装
pip install -r requirements.txt

# 或使用 pyproject.toml
pip install -e .
```

### 主要依赖

- `torch` - PyTorch深度学习框架
- `tensorflow` - TensorFlow（部分章节）
- `jupyterlab` - Jupyter环境
- `tiktoken` - 分词器
- `matplotlib` - 可视化
- `tqdm` - 进度条
- `numpy` - 数值计算
- `pandas` - 数据处理

## 📝 学习路径建议

### 阶段一：入门基础
1. 从 [llm-intro](llm-intro/) 开始，了解大语言模型基础概念
2. 学习 [pytorch](pytorch/) 掌握PyTorch基础操作
3. 学习 [attention](attention/) 理解注意力机制原理

### 阶段二：数据处理与模型实现
4. 学习 [data-engineering](data-engineering/) 掌握文本数据处理
5. 实现 [gpt-model](gpt-model/) 从零构建GPT模型

### 阶段三：模型训练
6. 进行 [pretraining](pretraining/) 预训练实践
7. 学习训练优化技巧和高级功能

### 阶段四：应用实践
8. 尝试 [fine-tuning](fine-tuning/) 各种微调方法
9. 探索LoRA等参数高效微调技术
10. 实践指令跟随和分类任务

## 🎯 项目特色

- ✅ **从零开始的完整实现** - 每个组件都有详细的实现代码
- ✅ **丰富的补充材料** - 包含大量实验和扩展内容
- ✅ **详细的代码注释** - 代码配有详细的中文注释和说明
- ✅ **交互式用户界面** - 提供多个交互式UI示例
- ✅ **性能优化技巧** - 包含训练和推理优化方法
- ✅ **多种模型架构** - 实现GPT、Llama、Qwen、Gemma等架构
- ✅ **完整的训练流程** - 从数据处理到模型部署的完整流程

## 📚 涵盖主题

- 注意力机制（Attention Mechanism）
- 字节对编码（BPE Tokenization）
- GPT模型架构
- 预训练（Pretraining）
- 微调（Fine-tuning）
- 指令跟随（Instruction Following）
- 分类任务（Classification）
- 参数高效微调（LoRA）
- 直接偏好优化（DPO）
- KV缓存优化
- 多GPU分布式训练
- 模型架构转换（GPT → Llama）

## 📄 许可证

详见 [LICENSE.txt](LICENSE.txt)

## 🤝 贡献

欢迎提交问题和改进建议！

---

**注意**：本项目为学习笔记和代码实现，适合想要深入理解大语言模型原理和实践的开发者。建议按照学习路径循序渐进，每个章节都包含丰富的实践代码和补充材料。
