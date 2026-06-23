# Causal Self-Attention — Interactive Demo

A fully self-contained, zero-dependency interactive explainer for causal 
self-attention — the core mechanism inside GPT-style decoder transformers.

Built as a single HTML file (~1,800 lines), it walks through the full 
attention pipeline in six sections:

1. **Concept** — what Q, K, and V projections mean and why the formula works
2. **Animated pipeline** — step through every stage: embeddings → Q/K/V 
   projection → raw scores → scaling → causal mask → softmax → weighted V sum
3. **Interactive token explorer** — type your own sentence, click any token 
   as the query, and watch the attention fan, score matrix, and Q·K dot-product 
   trace update live
4. **Causal mask visualiser** — see the lower-triangular mask that enforces 
   no future leakage, with the −∞ → 0 softmax logic made explicit
5. **Multi-head attention** — browse 12 simulated heads (syntactic, positional, 
   semantic, coreference), each with a mini heatmap preview and a full 
   interactive attention matrix
6. **Scaling factor** — drag a d_k slider and watch softmax sharpen or flatten 
   with and without the 1/√d_k correction

Temperature is adjustable throughout, and a step-by-step guided walkthrough 
introduces each concept. Inspired by [nanoGPT](https://github.com/karpathy/nanoGPT) 
and the original ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) paper.

**[Live demo →](https://rimas-codes.github.io/causal_attention_demo/)**
