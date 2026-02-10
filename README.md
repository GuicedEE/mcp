# GuicedEE MCP Server

MCP server implementation for GuicedEE with Java 25 and Vert.x 5.

- Hosted target endpoint: `https://mcp.guicedee.com/mcp`
- Protocol revision target: `2025-11-25`
- Transport support: Streamable HTTP and stdio
- Capability surface: tools, resources, prompts, completion

## Rules Repository Adoption

This project consumes the Rules Repository as a submodule at `rules/`.

- Initialize submodule:

```bash
git submodule update --init --recursive
```

- Primary references:
  - `rules/RULES.md`
  - `rules/AGENTS.md`
  - `rules/skills.md`

## Project Documents

- Pact: `PACT.md`
- Glossary: `GLOSSARY.md`
- Project Rules: `RULES.md`
- Guides: `GUIDES.md`
- Implementation: `IMPLEMENTATION.md`
- Prompt seed: `docs/PROMPT_REFERENCE.md`
- Architecture index: `architecture/README.md`

## Selected Stack

- Java 25 LTS
- Maven
- Vert.x 5
- GuicedEE lifecycle mapping
- Fluent API strategy: CRTP
- Logging: Log4j2
- Nullness: JSpecify

## Local Run

```bash
mvn -B -ntp test
mvn -B -ntp package
```

Set runtime values via `.env.example`.

## MCP Configuration Snippet

A generic MCP config is provided at `.mcp.json` and includes:

- Mermaid MCP server
- Hosted GuicedEE MCP endpoint

## Stage Gate Policy

- Docs-first stage gating is enabled.
- This project run defaults to optional stage approvals.
- Junie sessions auto-approve stage gates.
