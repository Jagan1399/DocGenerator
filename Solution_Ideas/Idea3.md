Option 3 – Hybrid MCP + External Tooling
Architecture:
Use existing static analysis/documentation tools (e.g., Sphinx for Python, JSDoc for JS, Doxygen for C++).
MCP server acts as a meta-orchestrator:
Detects language → picks appropriate tool.
Runs the tool → collects docs.
Post-processes into a uniform structured format.
Builds repo-wide bottom-up docs.
Tech Stack:
MCP server + adapters for different tools.
Structured intermediate representation (e.g., JSON AST → docs).
Optional embeddings for semantic navigation.

Pros:
Leverages mature tools (fewer bugs, less reinventing the wheel).
Standard output (Markdown/HTML).
Faster to build MVP.

Cons:
Harder to unify styles across different tools.
Dependency hell (managing all toolchains).
Limited customization compared to custom AST parsing.