---
name: internet-search
description: Search the internet for real-time information, news, or general knowledge.
---

# Internet Search

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:
- **topic**: Required. The search query keywords (e.g., "Aakash Kargathara portfolio", "latest AI news").
- **mode**: Selection. Use "quick" for rapid search results or "deep" for comprehensive research including full-page content analysis. Defaults to "quick".

**Constraints:**
- Synthesize the findings into a clear, accurate answer with citations (URLs) for each key point.
- If no relevant results are found, inform the user and suggest alternative keywords.
- For news or time-sensitive events, prioritize results from the last 24-48 hours if available.
- Always provide the direct source URL for every piece of information used in your summary.
