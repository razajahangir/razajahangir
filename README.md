# Raza Jahangir

**AI Systems Engineer** · agents, RAG, and self-hosted AI infrastructure for production use.

**Build → Evaluate → Deploy → Monitor**

I work across the full lifecycle. That means designing the agent or retrieval pipeline, testing it against real data before release, running it as a reliable service, and tracking quality, cost, and latency once it's live.

Before AI, I spent 13+ years as a backend engineer building PHP applications, WordPress plugins, CodeIgniter apps, APIs, and databases, plus web scraping in Python. That background shapes how I build AI systems: clean data pipelines, stable integrations, and code that is easy to maintain after launch.

---

### Focus

- **Agents** — multi-step workflows with tool calling, state, memory, and human-in-the-loop steps (LangGraph)
- **RAG** — ingestion, chunking, hybrid search, re-ranking, cited answers (LlamaIndex, pgvector)
- **Evaluation** — test sets and regression checks before release (LangSmith)
- **Deployment** — FastAPI services, self-hosted models, tracing, cost and latency tracking

### Stack

**AI / Python:** `Python` `LangGraph` `LangChain` `LlamaIndex` `LangSmith` `FastAPI` `LiteLLM` `Ollama`
**Data:** `PostgreSQL + pgvector` `Supabase` `MySQL`
**Web & infra:** `Node.js` `Next.js` `PHP` `WordPress` `Docker` `Cloudflare Tunnel`

---

### Projects

#### [inhouse-ai](https://github.com/razajahangir/inhouse-ai) · open source
A self-hosted, private AI stack for teams that want to run AI on their own hardware without sending data to third parties.
Runs on anything from a CPU-only laptop to large GPU servers.

- Chat UI: Open WebUI
- Model gateway: LiteLLM
- Local models: Ollama
- Document search: PostgreSQL + pgvector
- Secure remote access: Cloudflare Tunnel
- Benchmarked on consumer hardware

#### [DraftCraft](https://wordpress.org/plugins/draftcraft) · open source · [source](https://github.com/ArtisansWP/DraftCraft)
WordPress plugin that generates scheduled blog drafts in a site's brand voice.

- Bring-your-own-key through OpenRouter
- Review queue: nothing publishes without approval
- SEO sync with Rank Math, Yoast, and AIOSEO

#### Atlas Planner · client work
AI goal planning for a membership community.

- RAG over the client's coaching content
- JSON-schema structured outputs
- Server-side AI calls with cost controls

#### Custom GPT Manager · client work
Create and run multiple AI chat agents from the WordPress admin.

- Per-agent prompt, model, and output format
- Any model through OpenRouter
- Conversation and token logging, per-user rate limits

<sub>Client code is private. Reviews for both client projects are on [Upwork](https://www.upwork.com/freelancers/developerraza).</sub>

---

### In progress

- **Intelara** — bring-your-own-key LLM app with a custom RAG pipeline built without frameworks · `Next.js` `Supabase` `pgvector`
- **AgenticLearn** — helps developers close specific knowledge gaps instead of taking full courses · `FastAPI` `LangGraph` `LlamaIndex` `pgvector`

---

### Contact

[LinkedIn](https://www.linkedin.com/in/raza-jahangir) · [Upwork](https://www.upwork.com/freelancers/developerraza)
