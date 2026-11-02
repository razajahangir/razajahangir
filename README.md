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

**AI / Python:** `Python` `LangGraph` `LangChain` `LlamaIndex` `LangSmith` `FastAPI` `LiteLLM` `Ollama`<br>
**Data:** `PostgreSQL + pgvector` `Supabase` `MySQL`<br>
**Web & infra:** `Node.js` `Next.js` `PHP` `WordPress` `Docker` `Cloudflare Tunnel`

---

### Projects

#### [inhouse-ai](https://github.com/razajahangir/inhouse-ai) · open source
A self-hosted, private AI stack for teams that want to run AI on their own hardware without sending data to third parties.
Runs on anything from a CPU-only laptop to large GPU servers.

- One Docker Compose file: Open WebUI, LiteLLM gateway, Ollama, PostgreSQL + pgvector, Cloudflare Tunnel
- Document Q&A with citations; each user's knowledge bases are isolated
- No inbound ports open; identity check before the login page
- Python benchmark tool measuring time to first token and tokens/s on your own hardware
- Upgrade path to vLLM on bigger GPUs by changing only the gateway config

#### [DraftCraft](https://wordpress.org/plugins/draftcraft) · open source
WordPress plugin that generates scheduled blog drafts in a site's brand voice.

- Bring-your-own-key through OpenRouter
- Review queue: nothing publishes without approval
- SEO sync with Rank Math, Yoast, and AIOSEO

#### [Atlas Planner](https://www.upwork.com/freelancers/developerraza?p=2113898981690503168) · client work
AI goal-planning platform for a coaching membership community (WordPress + BuddyBoss). Members take a life & business assessment, get AI-recommended focus areas and goals, and turn them into scheduled actions. MVP built in 8 weeks, then developed in weekly releases for seven more months.

**AI layer**
- OpenAI ranks focus areas from assessment scores and proposes SMART goals and actions, retrieved from the client's goal and action library
- Weekly check-in analysis that generates short nudges and reschedule suggestions
- Every response follows a JSON schema, is validated in PHP before saving, and is retried if invalid; tool calling for goal selection
- All calls go through a server-side proxy; prompts and schemas are versioned in the repo with unit tests
- Cost controls: per-call token budgets, input truncation, retries with backoff on 429/500
- Telemetry per call (model, tokens, latency, estimated cost) in an admin view
- AI kill switch that falls back to rules-based suggestions; PII stripped before sending, plus a "delete my AI data" option

**Platform**
- Recurring actions with RRULE, timezone and DST safe; due date and recurrence rule enforced as mutually exclusive at the API and database layers
- Background jobs with Action Scheduler: hourly reminders, daily digests, weekly check-ins
- REST API, custom database tables, Elementor widgets
- Integrations: BuddyBoss notifications, ActiveCampaign email/SMS and CRM sync, GamiPress points and streaks
- Exports to PDF, iCal, and CSV

#### [Custom GPT Manager](https://www.upwork.com/freelancers/developerraza?p=2113899795565277184) · client work
WordPress plugin for building and deploying multiple custom GPTs from wp-admin, each with its own knowledge base, access rules, and ChatGPT-style chat UI. Built end to end, then extended over six months.

**AI layer**
- Per-GPT configuration: system prompt, model, temperature, token limit, and output format (text or JSON)
- Provider abstraction layer; any major model through OpenRouter
- Knowledge bases per GPT: file ingestion (PDF, DOCX, CSV, TXT) and URL/sitemap crawling, processed in background jobs
- Retrieval-grounded answers with citations; a content coach agent that parses the site's Elementor pages and links back to its sources
- Streaming responses through a server-side proxy; API keys never reach the browser
- Moderation filters before and after each response: blocklists, regex rules, jailbreak protection

**Platform**
- Access by role or membership level; rate limits and quotas per user, role, and GPT, with cool-downs
- Analytics per GPT and per user: conversations, tokens, spend, response time, errors, with CSV export
- Email and Slack alerts for error spikes and quota thresholds
- Data retention windows and deletion of a user's conversations
- Config import/export; multiple GPTs per page with isolated state, embedded via shortcode

<sub>Client code is private. Both projects were delivered across four contracts, all rated 5★ on [Upwork](https://www.upwork.com/freelancers/developerraza).</sub>

---

### In progress

- **Intelara** — bring-your-own-key LLM app with a custom RAG pipeline built without frameworks · `Next.js` `Supabase` `pgvector`
- **AgenticLearn** — helps developers close specific knowledge gaps instead of taking full courses · `FastAPI` `LangGraph` `LlamaIndex` `pgvector`

---

### Contact

[LinkedIn](https://www.linkedin.com/in/raza-jahangir) · [Upwork](https://www.upwork.com/freelancers/developerraza)
