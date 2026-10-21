### Hi, I'm Faizan

**I build LLM systems, then measure whether they actually work.**

I'm a data scientist working on retrieval-augmented generation (RAG), AI agents and LLM evaluation. Each project below is tested against a ground truth, reports what it costs, and says where it fails.

---

#### [Conversation Auditor](https://github.com/innovatewithfaizan/agent-conversation-auditor) · [live app](https://innovatewithfaizan.github.io/agent-conversation-auditor/)

Checks customer-support conversations against a written policy and cites the exact turn behind every finding.

- Caught **42 of 50** planted policy violations across 80 conversations (84%, 95% CI 73–93%)
- **No false alarms** on 15 near-misses built to look like violations
- An agent searching with tools caught 70%; fixed retrieval caught 52%
- **$0.0046** per conversation. Weak spot: it over-flags, and the README breaks down where

`Python` `OpenAI` `ChromaDB` `FastAPI` `agentic RAG` `LLM evaluation`

#### [Film content ratings from subtitles](https://github.com/innovatewithfaizan/Agentic-Retrieval-Augmented-Generation-for-AI-Powered-Content-Moderation)

Reads a film's subtitles and rates violence, sex, language and drug use for parents. Built three ways and tested on 75 films against published parent-guide reviews.

- **92%** of ratings are exact or one step off the parent guide
- **95–98%** of the quotes it gives as evidence really exist in the subtitles
- Strongest on language (up to 71% exact). Violence and drinking are hard, because they are seen rather than heard
- $0.004–$0.006 per film with gpt-5-mini

`Python` `OpenAI` `ChromaDB` `Streamlit` `RAG` `LLM-as-a-judge`

#### [Groundwork](https://github.com/innovatewithfaizan/groundwork) (formerly DocuFlow)

A modular RAG service that answers questions about your documents with citations, compares PDFs and extracts metadata.

- Retrieval finds the evidence for **22 of 25** test questions (88%), re-measured in CI on every change
- Contextual compression cuts the context sent to the LLM by **42%** and keeps 21 of those 22 hits
- 75 offline tests; Docker image and a manually triggered AWS ECS Fargate deploy

`Python` `FastAPI` `LangChain` `FAISS` `Docker` `GitHub Actions` `AWS`

---

#### How I work

- **Measure before claiming.** Every result above has a stated method, a sample size and something to compare against.
- **Show the failures.** Each README has a section on its limits and what the system gets wrong.
- **Ship it properly.** Tested code you can run, not just a notebook.
