# ML Infrastructure Demos

Interactive, in-browser demos of production ML-systems patterns — built as a
portfolio site and hosted with GitHub Pages at
https://peppercatmeow.github.io/personal.

- **RAG service with an eval harness** (`rag/`) — hybrid BM25 + TF-IDF
  retrieval over a document corpus, tunable chunking, and an eval harness
  (P@k / R@k / MRR) with baseline snapshots for before/after config comparison.
- **Autoscaled LLM inference endpoint** (`inference/`) — discrete-event
  simulation of a serving fleet: continuous batching, queue dynamics, a
  KV-cache memory calculator, and a latency-driven autoscaler with
  cost-per-token readout.
- **LoRA fine-tune: before/after benchmarks** (`lora/`) — exact
  trainable-parameter accounting across ranks and target modules, full-FT vs
  LoRA vs QLoRA memory math, base vs LoRA vs RAG benchmark charts, and a
  "which lever do I pull" decision guide.

Every page is a single self-contained HTML file — no build step, no CDN
dependencies, no backend. The retrieval, scheduling, and parameter math are
real algorithms running client-side on toy-scale data; each page labels
where it simulates.
