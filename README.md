# AI Data Tools

AI-powered intelligence tools deployed on [Apify](https://apify.com/harmony_labs).
One input in, a structured, actionable report out. Pay-per-use. No API keys. MCP-compatible.

## Projects

### Head-to-Head Competitor Analysis
- **What it does:** Paste your URL and a competitor's URL → get back a neutral, 7-section comparative brief (positioning, pricing, feature gaps, messaging, tech stack, key differences) in 1–3 minutes
- **Stack:** Python, web crawling, LLM API (Gemini 2.5 Flash / Claude Haiku 4.5), Apify SDK
- **Live:** [apify.com/harmony_labs/head-to-head-competitor-analysis](https://apify.com/harmony_labs/head-to-head-competitor-analysis)
- **How it works:** Crawls up to 10 pages of each site (prioritizing /about, /pricing, /features, /customers, /blog), sends both content sets to an LLM with a structured comparative prompt, and returns a styled HTML report plus plain text. Tech stack is detected from visible signals (scripts, meta tags, mentions).

### AI Keyword Generator
- **What it does:** One seed keyword in → ranked list of long-tail keywords out, each tagged with search intent (informational / commercial / transactional) and a 1–10 difficulty score
- **Stack:** Python, LLM API (Gemini 2.5 Flash / Claude Haiku 4.5), Apify SDK
- **Live:** [apify.com/harmony_labs/ai-keyword-generator](https://apify.com/harmony_labs/ai-keyword-generator)
- **How it works:** Sends the seed keyword to an LLM with a structured output schema that forces intent classification and difficulty estimation. Returns one row per keyword as clean JSON in the dataset.

### Competitor Intelligence Report
- **What it does:** Paste a competitor's URL → get back who their customers are, what tech they run, how they position, and 3–5 specific exploitable gaps in ~2 minutes
- **Stack:** Python, web crawling, LLM API (Gemini 2.5 Flash / Claude Haiku 4.5), Apify SDK
- **Live:** [apify.com/harmony_labs/competitor-intel-report](https://apify.com/harmony_labs/competitor-intel-report)
- **How it works:** Crawls up to 5 pages of the target site (prioritizing /customers, /case-studies, /testimonials, /about, /pricing), passes the extracted content to an LLM with a structured prompt that forces gap analysis against stated positioning, and returns a categorized report with named customers, tech stack, and specific opportunities.

## Common Design Principles

- **Structured output, not freeform text** — every actor returns typed, parseable JSON (or styled HTML for reports)
- **No API keys** — LLM calls routed through Apify's OpenRouter proxy
- **MCP-compatible** — all three actors can be called as tools from any MCP client
- **Pay-per-use** — no subscriptions, no minimums

## About

Building AI-native intelligence tools. Focused on competitive analysis, structured extraction, and LLM-powered research workflows.   
