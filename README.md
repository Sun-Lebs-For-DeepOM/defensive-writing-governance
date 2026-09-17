# Defensive Writing Governance

`defensive-writing-governance` is a lightweight Codex plugin for separating defensive writing from reader-facing prose.

Its core skill, `defensive-writing-governance`, works alongside an existing writing task:

- the original task continues to produce the document;
- disclaimers, pre-emptive defenses, capability notes, and process-oriented self-protection are routed to a separate governance file;
- substantive assumptions, evidence limits, uncertainty, risk information, and required disclosures remain in the document.

## Modes

### Preventive governance

For a new writing task, the skill creates or reuses `writing-governance.md` before drafting. Defensive content is recorded there instead of being shown to readers.

### Existing-draft governance

For an existing draft, the skill moves defensive content to the governance file while preserving the draft's facts, reasoning, structure, evidence strength, and commitments.

## Plugin structure

```text
defensive-writing-governance/
├── .codex-plugin/
│   └── plugin.json
└── skills/
    └── defensive-writing-governance/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── assets/
            └── writing-governance.md
```

## Use

After installing the plugin, invoke the skill with a writing task:

```text
Use $defensive-writing-governance for this draft. Keep substantive limits in the document and place defensive content in the governance file.
```

The plugin contains no MCP server, external application, or network dependency.

## License

MIT
