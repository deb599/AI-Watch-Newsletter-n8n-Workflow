# AI-Watch-Newsletter-n8n-Workflow
The workflow leverages multi-agent orchestration to handle content curation, analysis, and summarisation efficiently. Each agent has a specialised role, allowing the system to operate dynamically and produce high-quality insights.

***

## Overview

**AI Watch** automates the discovery, curation, and summarization of AI-related news and policy updates. Built with **n8n** and enhanced through **multi-agent AI orchestration**, the workflow intelligently monitors RSS feeds, classifies content by risk relevance, and prepares structured summaries suitable for newsletters, LinkedIn updates, and dashboards.

This repository focuses on **showcasing orchestration logic, not code distribution**. It outlines how the workflow blends retrieval, classification, and narrative generation in a scalable, no-code format.

## Purpose

The goal is to **show how AI risk monitoring can be automated** with minimal technical intervention—turning large RSS streams into **contextual, high-signal summaries** for policy analysts, founders, and AI safety researchers.

## How It Works

1. **Trigger and Fetch**  
   - Inputs determine the time horizon for collecting RSS data.  
   - The workflow fetches new items from configurable feeds listed in Google Sheets.

2. **Filter and Classify**  
   - Each article passes through risk-level filtering using curated keyword clusters.  
   - The system categorizes topics into risk, ethics, governance, or opportunity areas.

3. **Summarize and Structure**  
   - Summaries are generated using AI-powered agents with assurance-driven prompts.  
   - Classified items are formatted into short insight bullets and long-form commentary drafts.

4. **Output and Sync**  
   - Results are sent to Google Sheets for tracking and optionally to publishing nodes (LinkedIn drafts, Google Docs, or newsletter queues).  
   - Each cycle can run manually or on schedule.

## Key Features

- End-to-end **RSS ingestion** and parsing  
- **AI-assisted classification** tuned to risk and opportunity themes  
- Multi-agent orchestration for **summarization and theme extraction**  
- Seamless integration with **Google Sheets and Docs APIs**  
- Modular design allowing feed, prompt, and category updates

## Architecture At A Glance

| Module | Description |
|--------|--------------|
| Feed Fetcher | Reads source data via RSS and filters duplicates |
| Parser & Filter | Extracts key risk indicators based on keyword heuristics |
| Classifier Agent | Assigns risk category and impact relevance |
| Summarizer Agent | Produces brief and long-form summaries |
| Output Layer | Synchronizes structured results into Sheets, Docs, or publishing tools |

## Multi-Agent Highlights

The workflow uses independent **AI nodes** to ensure layered reasoning and output quality, **with human-in-the-loop review for every output**:

- **Summarization Agent:** Converts raw content to technical and non-technical abstracts.  
- **Blog Review Agent:** Refines writeups into Substack-ready or newsletter-friendly copy.  
- **Hook Generator Agent:** Creates emotionally engaging one-liners for visibility.  
- **Ask AI Prompt Generator:** Suggests practical AI exploration tasks derived from each insight.
- **Image Generation Agent:** Produces a relevant visual to accompany each article.

## Use Cases

- Weekly insight digests or curated newsletters  
- LinkedIn or Substack post preparation from structured summaries

## Security and Privacy

Sensitive credentials—API keys, auth tokens, and connectors—are user-configured within n8n’s secure credential store. The repository **does not** include private APIs, datasets, or workflow JSONs.

## Output and Links

- **Newsletter Link:** [AI Watch newsletter](https://watchera.substack.com/) — delivers concise, curated AI insights with summaries, hooks, prompts, and visuals ready to publish every Saturday at 3 PM.

## N8n flow
<img width="1131" height="575" alt="Screenshot 2025-10-18 at 10 50 09 am" src="https://github.com/user-attachments/assets/c468b948-a1f2-4eed-8010-802e554fe0bc" />


***

### About the Author

**Debasmita Mukherjee** specializes in AI automation orchestration and AI risk content pipelines.
This showcase reflects her ongoing research into **Responsible AI horizon scanning**, no-code AI operations, and **futurist content automation** frameworks.

