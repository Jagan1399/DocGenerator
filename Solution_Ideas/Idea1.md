Option 1 – Monolithic MCP Server (All-in-One)
Architecture:
One MCP server that directly:
Scans the repository (filesystem or Git integration).
For each file: parses syntax → extracts functions/classes/modules → generates docs.
Stores docs in a structured format (e.g., JSON or Markdown in a docs/ folder).
Builds higher-level repo docs (bottom-up aggregation).
Tech Stack:
MCP server (Python/Node)
File parsers (e.g., ast for Python, tree-sitter for multi-language)
Vector/embedding store (optional, for semantic search)
Markdown/HTML generator

Pros:
Simpler to implement and deploy.
Straightforward for small–medium repos.
Easy to plug into an LLM for contextual answers.

Cons:
Harder to scale for huge repos.
Limited flexibility in swapping out analyzers per language.
