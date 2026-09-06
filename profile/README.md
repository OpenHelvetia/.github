# OpenHelvetia

A Swiss association ([openhelvetia.swiss](https://openhelvetia.swiss)) that builds the interface which makes the Confederation's machine-readable data holdings — Fedlex, LINDAS, opendata.swiss and more — efficiently usable for AI systems, and keeps the directory for it. The data stays with the organisations that publish it. What you find here are the modules, one repository each, published from the association's corpus as they become ready.

## The modules

| Layer | Module | Repository | State |
|---|---|---|---|
| L0 · Standard and register | Manifest standard, validator, seal register, agent-card tools | [standard-manifest-oh](https://github.com/OpenHelvetia/standard-manifest-oh) | draft |
| L1 · Directory and verification | Checker (`oh-check`): probes, history, badges | [checker-oh](https://github.com/OpenHelvetia/checker-oh) | prepared |
| L2 · Machine access | MCP server over Fedlex (Swiss federal law, 35 tools) | [mcp-fedlex-oh](https://github.com/OpenHelvetia/mcp-fedlex-oh) | prepared |
| L2 · Machine access | MCP server over the political data cubes in LINDAS (8 tools) | [mcp-lindas-politics-oh](https://github.com/OpenHelvetia/mcp-lindas-politics-oh) | prepared |
| L2 · Machine access | API spine: fourteen operations, spec from code, generated client, passkey login | [api-spine-oh](https://github.com/OpenHelvetia/api-spine-oh) | prepared |
| L2 · Machine access | MCP gateway: one policy boundary (budget, rate limit, typed refusals) over the registry tools and both domain servers, MCP streamable HTTP and a JSON door | [mcp-gateway-oh](https://github.com/OpenHelvetia/mcp-gateway-oh) | operated |
| L5 · User view | Citizen chat: UI-free core with the deterministic check of quotations, keys and figures, provider table, Dioxus shell compiled to WebAssembly | [chat-oh](https://github.com/OpenHelvetia/chat-oh) | operated |
| L2 · Machine access | A2A agent transport | with a later publication | prepared |

The states are the six words of the platform's [state vocabulary](https://openhelvetia.swiss/en/docs/reference/state-words/); what each module is, how to run, test and call it, is on its card and guide on the website: [Infrastructure](https://openhelvetia.swiss/en/directory/) · [Documentation](https://openhelvetia.swiss/en/docs/).

## How the repositories are named

Every repository ends in `-oh`: it is the association's own build over a public holding, never the holding itself. What the name says before that is the protocol and the slice of the holding it covers — `mcp-lindas-politics-oh` is the MCP server over the *political* cubes in LINDAS, not over LINDAS as a whole.

## How to read these repositories

- Every repository builds and tests on its own, offline, from recorded fixtures: `cargo test --locked --manifest-path <crate>/Cargo.toml`.
- Each README says at the bottom which corpus commit it was published from. Changes go through the corpus and arrive with the next publication; issues here are welcome.
- Security reports, in confidence: admin@openhelvetia.swiss.

## Licence

Apache-2.0, unless a repository says otherwise.
