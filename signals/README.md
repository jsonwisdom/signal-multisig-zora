# Signal Tracking v0

This directory records time-series observations of the Digital ABI Domain.

## File: signal-log.jsonl
- Format: JSON Lines (one JSON object per line)
- Mode: append-only

## Minimal Schema
```
{
  "timestamp_utc": "ISO8601",
  "source": "manual|script",
  "type": "system_pulse|gateway_check|proof_update|base_tx",
  "status": "green|yellow|red",
  "watcher_cid": "ipfs cid",
  "proof_cid": "ipfs cid",
  "base_tx": "0x...",
  "note": "free text"
}
```

## Rules
- Never edit past lines
- Only append new entries
- Each entry represents an observable event

## Purpose
Convert static proof into a time-series of verifiable system states.
