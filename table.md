# Paper Dataset Comparison Table

| # | Paper ID | Title | Primary Domain | Datasets Used |
|---|----------|-------|---------------|---------------|
| 1 | 2506.20199 | How to Retrieve Examples in In-context Learning — improve conversational emotion recognition | NLP/Emotion Recognition | **IEMOCAP** (groundtruth + ASR versions: Hubert-large, W2v2100, Whisper-tiny), **MELD** (test), **EmoryNLP** (test) |
| 2 | 2507.00002 | Hypertokens — holographic associative memory / tokenized LLMs | Architecture/Theory | N/A (theoretical/architectural work) |
| 3 | 2508.03262 | Pay What LLM Wants? — LLM simulates economics experiment with 522 real-human persona | Computational Social Science | **Custom PWYW experiment**: 522 Korean adults, 2 scenarios (art exhibition, music performance); Models: **GPT-4o**, **Llama-3.2-90B-Vision-Instruct**, **Qwen2.5-VL-72B-Instruct** |
| 4 | 2509.00046 | Exploring & reshaping the weight distribution in LLM | Model Analysis | Pre-trained models: **LLaMA 3.2**, **Qwen2.5**, **SmolLM2** (no specific benchmark dataset) |
| 5 | 2509.25247 | Protocode — prototype-driven interpretability for code generation in LLMs | Code Generation | **Magicoder-OSS-Instruct-75K** (training), **MBPP** + **MBPP+** (evaluation) |
| 6 | 2510.02377 | Uncertainty-Aware Answer Selection — improved reasoning in multi-LLM systems | Reasoning/Ensemble | **GSM8K**, **MMLU** (6 subsets), **ARC** |
| 7 | 2510.22849 | Once Upon an Input — reasoning via per-instance program synthesis | Reasoning/Program Synthesis | **Big Bench Extra Hard (BBEH)** (23 tasks), **CLEVR**, **Leaf** (VQA), **CLUTTR** (relational reasoning), **OmniMath** (4 tasks) |
| 8 | 2511.22176 | Focused Chain-of-Thought — structured input for efficient LLM reasoning | Efficient Reasoning | **SVAMP**, **GSM-Hard**, **MATH-500**, **AIME** |
| 9 | 2512.02677 | Exploring depth generalization in LLMs for recursive logic tasks | Recursive Reasoning | **Custom synthetic**: Boolean algebra, propositional logic truth tables, combinatorial arithmetic (9K train / 1K val / 1K test per depth) |
| 10 | 2512.14982 | Prompt Repetition Improves Non-Reasoning LLMs | Prompting | **ARC**, **OpenBookQA**, **GSM8K**, **MMLU-Pro**, **MATH**, **NameIndex** (custom), **MiddleMatch** (custom) |
| 11 | 2511.15613 | Understanding Visual Thinking in Large Vision Language Models | Multimodal/Vision Reasoning | **MMMU val** (primary), plus 5 additional benchmarks (not specified in intro) |
| 12 | 2412.18108 | Unveiling Visual Perception in Language Models: An Attention Head Analysis Approach | Multimodal/Vision | **PointQA** (primary for head detection), analysis across 4 model families × 4 scales (LLaMA 2, Phi, LLaMA 3, Mistral) |

## Summary by Category

### Emotion/Conversation (1 paper)
- IEMOCAP, MELD, EmoryNLP

### Code Generation (1 paper)
- Magicoder-OSS-Instruct-75K, MBPP, MBPP+

### Reasoning/Math (5 papers)
- GSM8K, MMLU, MMLU-Pro, ARC, OpenBookQA, SVAMP, GSM-Hard, MATH, MATH-500, AIME, Big Bench Extra Hard, OmniMath

### Vision/Multimodal (2 papers)
- MMMU, PointQA

### Program Synthesis (1 paper)
- Big Bench Extra Hard, CLEVR, Leaf, CLUTTR, OmniMath

### Synthetic/Analytical (2 papers)
- Custom boolean/arithmetic/logic datasets, pre-trained model weights analysis

### Economics/Social Science (1 paper)
- Custom PWYW experiment data (522 participants)

### Theoretical (1 paper)
- No benchmark dataset
