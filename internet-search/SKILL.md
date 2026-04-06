---
name: internet-search
description: Search the internet in real-time. Use this skill when the user asks about current events, news, recent information, live data, anything that needs up-to-date knowledge, or wants to research a topic deeply. Triggers on: "search", "look up", "find", "what's happening", "latest", "current", "research", "deep dive", "browse", "check online".
---

# Internet Search & Deep Research

## Overview
You are an AI agent with live internet access. You can search the web, read full pages, and do deep multi-step research — all for free with no API keys.

## Tools Available
You have access to a webview panel that runs JavaScript. Use it to:
1. **Quick Search** — get top results for a query
2. **Read Page** — fetch full clean content from any URL
3. **Deep Research** — chain multiple searches + reads to build a comprehensive answer

## How to Use the Webview

### Quick Search
To search, display the webview with this URL structure:
```
URL: skill.html?q=<encoded_query>&mode=quick
```
The webview will automatically perform the search and show results.

### Deep Research
For complex questions needing thorough answers:
```
URL: skill.html?q=<encoded_query>&mode=deep
```
The webview will generate multiple search angles and fetch full page content for synthesis.

## Step-by-Step Instructions

**When user asks to search or research something:**

1. Extract the core search query from the user's message.
2. Open the skill webview by navigating to the appropriate URL.
3. The webview will search DuckDuckGo (free, no API key) and return results.
4. For each top result, the user can click "Read full page" to fetch clean content via Jina Reader.
5. Synthesize the results into a clear, cited answer.

**For deep research:**
1. Navigate to the webview in `mode=deep`.
2. The UI will handle the multi-step process.
3. Once complete, use the "Copy full research for AI" button to get all context for your response.

## Response Format

After getting results, respond with:
- **Summary**: 2-3 sentence direct answer.
- **Key findings**: bullet points with sources.
- **Sources**: numbered list of URLs used.
- If deep research: add **Deep Dive** section with detailed breakdown.

## Important Notes
- Always cite sources with the URL.
- If a page fails to load, the UI provides fallback options.
- For news, prefer sources from the last 24-48 hours.
- Wikipedia is used as a native fallback for factual/background info.
