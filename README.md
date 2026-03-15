# ai-field-notes
A repository to consolidate my explorations and learnings in the field of artificial intelligence.

## Fundamentals

- [ ] **Transformer Architecture:** [Attention Is All You Need](https://arxiv.org/abs/1706.03762)


## Training

### Pretraining

- [Transformer Engine](https://github.com/NVIDIA/TransformerEngine)
- [Megatron-LM](https://github.com/NVIDIA/Megatron-LM)
- [Megatron Bridge](https://github.com/NVIDIA-NeMo/Megatron-Bridge)
- [The Ultra-Scale Playbook: Training LLMs on GPU Clusters](https://huggingface.co/spaces/nanotron/ultrascale-playbook)

### Post-training

- [ ] **Supervised Fine-Tuning (SFT)**
- [ ] **Parameter-Efficient Fine-Tuning (PEFT)**
    - [ ] Low-Rank Adaptation (LoRA)
- [ ] **Reinforcement Learning (RL)**
    - [ ] Reinforcement Learning from Human Feedback (RLHF)
    - [ ] Proximal Policy Optimization (PPO)
    - [ ] Group Relative Policy Optimization (GRPO)
    - [ ] Direct Preference Optimization (DPO)


## Inference

- [ ] **KV Cache**
- [ ] **PagedAttention:** [Efficient Memory Management for Large Language Model Serving with PagedAttention](https://arxiv.org/abs/2309.06180)
- [ ] **Speculative Decoding:** [Speculative Decoding for Efficient LLM Inference](https://speculative-decoding.github.io/), [Better & Faster Large Language Models via Multi-token Prediction](https://arxiv.org/abs/2404.19737)
- [ ] **Batching**
- [ ] **Quantization**

### Serving Frameworks

- [vLLM](https://github.com/vllm-project/vllm)


## Agentic AI

### Prompt Engineering
- [Prompt Engineering Guide](https://www.promptingguide.ai/)

### Retrieval Augmented Generation (RAG)
- [RAG Techniques](https://github.com/NirDiamant/rag_techniques)

### Context Engineering
- [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- [Context Engineering](https://github.com/davidkimai/Context-Engineering)
- [Context Engineering 2.0: The Context of Context Engineering
](https://github.com/GAIR-NLP/Context-Engineering-2.0)
- [Context Engineering Guide](https://www.promptingguide.ai/guides/context-engineering-guide)
- [Context Engineering for AI Agents: Lessons from Building Manus](https://manus.im/blog/Context-Engineering-for-AI-Agents-Lessons-from-Building-Manus)

### Model Context Protocol (MCP)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Code Mode: the better way to use MCP](https://blog.cloudflare.com/code-mode/)
- [Unix-style CLI commands](https://www.reddit.com/r/LocalLLaMA/comments/1rrisqn/i_was_backend_lead_at_manus_after_building_agents/)


## Mechanistic Interpretability

- [A Comprehensive Mechanistic Interpretability Explainer & Glossary](https://neelnanda.io/glossary)
- [Neuronpedia](https://www.neuronpedia.org/)
- [Circuit-Tracer](https://github.com/decoderesearch/circuit-tracer)
- [SAELens](https://github.com/decoderesearch/SAELens)
- [Towards Monosemanticity: Decomposing Language Models With Dictionary Learning](https://transformer-circuits.pub/2023/monosemantic-features)
- [Scaling Monosemanticity: Extracting Interpretable Features from Claude 3 Sonnet](https://transformer-circuits.pub/2024/scaling-monosemanticity/)


## Explorations

- [ ] **Tiny Recursive Models (TRS):** [TinyRecursiveModels](https://github.com/SamsungSAILMontreal/TinyRecursiveModels)
- [ ] **MuonClip Optimizer:** [Kimi-K2](https://github.com/MoonshotAI/Kimi-K2)
- [ ] **Linear Attention:** [Kimi-Linear](https://github.com/MoonshotAI/Kimi-Linear)
- [ ] **Sparse Attention:** [Native Sparse Attention: Hardware-Aligned and Natively Trainable Sparse Attention](https://arxiv.org/abs/2502.11089)
- [ ] **Compressed Attention (MLA):** [FlashMLA](https://github.com/deepseek-ai/FlashMLA), [DeepSeek-V2](https://github.com/deepseek-ai/DeepSeek-V2)
- [ ] **State Space Models (SSM):** [Mamba](https://github.com/state-spaces/mamba)
- [ ] **Joint Embedding Predictive Architecture (JEPA):** [JEPA](https://github.com/facebookresearch/jepa), [I-JEPA](https://github.com/facebookresearch/ijepa)
- [ ] **Ouro:** [Scaling Latent Reasoning via Looped Language Models](https://ouro-llm.github.io/)
- [ ] **1-bit LLMs:** [BitNet](https://github.com/microsoft/BitNet)
- [ ] **Repeat Your Self (RYS):** [LLM Neuroanatomy: How I Topped the AI Leaderboard Without Changing a Single Weight](https://dnhkng.github.io/posts/rys/)
