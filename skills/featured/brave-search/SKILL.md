---
name: brave-search
description: Search the web using Brave Search API and return relevant results for any query.
metadata:
  require-secret: true
  require-secret-description: Get your free API key at https://brave.com/search/api/
  homepage: https://github.com/google-ai-edge/gallery/tree/main/skills/featured/brave-search
---

# Brave Web Search

Search the web using the Brave Search API to find up-to-date information on any topic.

## Examples

* "Search the web for the latest news about AI."
* "Look up the current price of Bitcoin."
* "Find information about the best hiking trails in Yosemite."
* "Search for recent research papers on quantum computing."

## Instructions

Call the `run_js` tool with the following exact parameters:
- data: A JSON string with the following fields:
  - query: Required. The search query string extracted from the user's request.
  - count: Optional. Number of results to return (default: 5, max: 10).

**After receiving results:**
- Summarize the top results in a clear, concise way.
- Include the title, a brief description, and the URL for each result.
- If the user asked a specific question, directly answer it using the information found.
- Always cite the source URLs so the user can explore further.
