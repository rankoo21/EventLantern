# Event Lantern

Event Lantern turns a public event page into a validator-agreed deadline receipt. The UI is a three-stage lantern path: register an event, resolve its source through consensus, then acknowledge the stored receipt.

## Contract

`contracts/checkpoint_graph.py` contains `DeadlineRelay`. It stores the owner, event name, HTTPS source, timezone hint, canonical status, extracted date, summary, and SHA-256 source digest. Lifecycle: `REGISTERED -> RESOLVED -> ACKNOWLEDGED`.

- Studionet contract: `0xd31de640F833B1232b070EB501Eb5f7b12C1E8bA`
- Live site: https://event-lantern-genlayer.pages.dev
- Public repository: https://github.com/rankoo21/EventLantern

## Checks

```text
python -m pytest tests -q
genvm-lint contracts/checkpoint_graph.py
npm run build
```
