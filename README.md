## Jesús Oñoro — AI Engineer / AI Architect

I build the infrastructure agents run on.

- **MCP** — 6 Model Context Protocol servers in production exposing ~394 tools, plus a multi-tenant MCP gateway.
- **LLM routing** — two multi-provider routers: 20 models across 9 providers, local→cloud escalation, credit-weighted billing, failover and a provider kill switch. KV-cache compression (PolarQuant + QJL) implemented from scratch.
- **Agent orchestration** — a five-tier autonomy loop, a Thompson-sampling task router that picks agents on capability match × historical reward, an A2A protocol over SSE, and human-in-the-loop approval gates with signed proposal tokens.
- **Evals** — a SWE-bench harness driving my own agent runtime, with a 7-tier pre-judge of my own design. Across 89 predictions: 100% well-formed patches, 84% exact file match, 74% correct region.
- **Retrieval** — hybrid BM25 + embedding RAG, local zero-network embeddings (Qwen3-Embedding-0.6B ONNX), pgvector in the cloud, and an agent memory system doing extraction, consolidation and contradiction detection.
- **Applied ML** — trained and shipped a wake-word classifier: source-level train/val split before augmentation, Adam + BCE, ONNX export, and a second-stage classifier that catches augmentation artefacts.

**Shipped, live on their own domains:** [ohwow.fun](https://ohwow.fun) (local-first AI runtime + cloud dashboard) · [aved.ai](https://aved.ai) (community platform) · [dplaza.io](https://dplaza.io) (multi-tenant on-chain commerce, Stripe Connect + USDC settlement on Base) · [studentcenter.io](https://studentcenter.io) (ERC-721 academic credentials on Base mainnet).

Over 28 months I authored 20,892 of 21,632 commits across these five platforms — schema and RLS through payments and on-chain settlement to the UI a customer touches. **Most of that work lives in private client repositories**, so the graph here shows the public slice.

**Stack** — TypeScript · Python · SQL · Kotlin · Solidity · Next.js · React · Node · PostgreSQL/Supabase (RLS) · SQLite · MCP · Claude Agent SDK · llama.cpp · ONNX Runtime · PyTorch · pgvector · Stripe Connect · Thirdweb / ERC-721 on Base · Vercel · Fly.io

Colombia (UTC−5), working US hours. English & Spanish.
📫 ogsus@ohwow.fun · [linkedin.com/in/jesusonoro](https://linkedin.com/in/jesusonoro)
