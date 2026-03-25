# DuckDuckGo Search Skill

Search the web and fetch URL content using DuckDuckGo (no API key required).

## Features

- Web search using DuckDuckGo
- URL content fetching and extraction
- JSON output for easy integration
- No API key required

## Prerequisites

```bash
pip3 install duckduckgo-search
```

## Installation

```bash
clawhub install duckduckgo-search-skill
```

## Usage

### In OpenClaw

This skill is automatically triggered when you search for information or fetch URLs.

### Command Line

```bash
# Search
python3 scripts/ddg_search.py "your search query" --max-results 10

# Fetch URL
python3 scripts/ddg_fetch.py "https://example.com" --timeout 30
```

## Output Format

### Search Results (JSON)
```json
{
  "query": "search query",
  "count": 10,
  "results": [
    {
      "title": "Result title",
      "url": "https://example.com",
      "snippet": "Description snippet"
    }
  ]
}
```

### Fetch Results (JSON)
```json
{
  "url": "https://example.com",
  "title": "Page Title",
  "text": "Extracted readable content...",
  "description": "Meta description",
  "status_code": 200,
  "error": null
}
```

## License

MIT
