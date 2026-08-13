# Penumbra Forge

**Security tooling for the AI-agent era.**

AI agents now install dependencies at machine speed, generate code that leaks credentials, and load third-party skills and instructions on the fly. Each of those is a new attack surface. Penumbra Forge builds focused, zero-dependency tools that defend them — fast enough to run on every commit, honest enough to trust the output.

---

### 🌳 [vexes](https://github.com/penumbraforge/vexes) — dependency supply-chain scanner

Cross-ecosystem vulnerability scanner with a 4-layer behavioral engine: AST code inspection, dependency-graph profiling, behavioral fingerprinting, and registry-metadata analysis on top of the OSV database. Reconstructs real supply-chain attacks (the axios RAT, Shai-Hulud, event-stream) to prove detection. Pre-install guard, verified fixes, SARIF for CI. **Zero dependencies.**

`npx @penumbraforge/vexes scan`

### 🔐 [gate](https://github.com/penumbraforge/gate) — secret scanner with auto-fix

Zero-config scanner that finds secrets, tells you how exposed they are (local / committed / pushed), and fixes them — extracting values to `.env` and rewriting the source. Entropy + rule detection, signed rule packs, a pre-commit hook, and a GitHub Action. Privacy by construction: findings are redacted by default and credential verification is opt-in.

`npx @penumbraforge/gate scan`

### 📚 [mcp-librarian](https://github.com/penumbraforge/mcp-librarian) — a signed skill supply chain for agents

An MCP server that gives coding agents a searchable library of skills — and treats those skills as a supply chain to secure. Quality-weighted BM25 search with progressive disclosure, Ed25519 signing with tamper detection on load, a prompt-injection content guard over both skills and fetched web content, and SSRF-hardened networking. **Zero dependencies.**

---

**Common thread:** deterministic tools you can run everywhere, with AI assistance layered on top — not bolted through the middle. Everything is open source, dependency-light, and built to fail loud rather than pass quietly.

[penumbraforge.com](https://penumbraforge.com) · Built by [Shadoe Myers](https://github.com/penumbraforge)
