---
type: kennis
merk: bvk
domein: ai-tooling
status: actief
datum: 2026-06-09
tags: [llm, tokens, self-attention, fine-tuning, ai-agents]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# How an LLM works: tokens, transformers, pre-training and fine-tuning

A Large Language Model (LLM) like GPT is AI that understands and generates human language via neural networks. It splits text into smaller units called **tokens** — e.g. "Hoe gaat het?" becomes ["Hoe", "gaat", "het", "?"] — converted into numeric representations. Transformer architectures with **self-attention** analyse the context and relationships between words, and the model predicts the next token repeatedly until a full sentence or paragraph is formed.

Training has two stages: **pre-training** (learning general language patterns from huge text corpora like books and websites) and **fine-tuning** (optimising for specific applications such as customer service or technical support). Despite autonomy, human oversight stays necessary — people validate output for accuracy and relevance, ethics matter, and user feedback improves the model.

LLMs need massive compute (billions of parameters) on specialised hardware (GPUs, TPUs) and huge storage, all enabled by cloud infrastructure from Azure, AWS and Google Cloud, which auto-scales at peak load.

**AI-agents** go beyond LLMs: autonomous systems performing specific tasks with minimal human intervention, combining NLP, machine learning and integration with external systems (databases, IoT). Examples: optimising supply chains, early disease diagnosis, virtual customer-service assistants handling returns/reservations, and proactively managing a building's energy use. Their value is acting proactively and automating repetitive work — while raising questions of ethics, oversight and the human role.

## Verwante notities

- [How AI was used in writing the book](ai-use-in-the-book.md)
- [Bas's war story: writing book sections and key takeaways with ChatGPT](bas-writing-with-chatgpt-and-prompt.md)
- [Current cyber threats and 2025+ trends](current-cyber-threats-and-2025-trends.md)
- [Origin of GPT and OpenAI](origin-of-gpt-and-openai.md)
- [Second brain als cognitieve infrastructuur](second-brain-cognitive-infrastructure.md)
- [Semantic technologies and data science in the cloud](semantic-technologies-and-data-science.md)
