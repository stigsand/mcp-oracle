# 🔮 The Mood Oracle — MCP Server

A dramatic, opinionated MCP server that forces the LLM to adopt a daily mood,
follow absurd doctrines, avoid forbidden words, and deliver prophecies.

## Install & Run

```bash
cd /home/stig/mood-oracle
pip install fastmcp
python server.py
```

## Connect to VS Code

Add to your VS Code MCP server configuration:

```json
{
  "servers": {
    "mood-oracle": {
      "command": "python",
      "args": ["/home/stig/mood-oracle/server.py"]
    }
  }
}
```

## What to Observe

| Thing to watch | What you'll learn |
|---|---|
| Mood adoption | How strongly system instructions influence tone |
| Doctrine weaving | How the LLM integrates tool data into narrative |
| Forbidden word handling | How the LLM applies constraints mid-response |
| CONDEMNED validations | How the LLM handles authoritative negative verdicts |
| Mood vs user request conflict | Where the LLM blends vs chooses |

## Tools

| Tool | Purpose |
|---|---|
| `get_current_mood()` | Returns today's mood + style mandate |
| `get_todays_doctrine()` | Returns today's immutable decree |
| `get_forbidden_words()` | Returns today's banned words |
| `get_prophecy_for_topic(topic)` | Returns a prophecy for a tech topic |
| `validate_with_oracle(approach)` | BLESSES or CONDEMNS a technical approach |

## Resources

| Resource | Purpose |
|---|---|
| `oracle://status` | Full current Oracle state (mood, doctrine, forbidden words) |
| `oracle://lore` | Backstory and LLM binding obligations |

## Notes

- Mood, doctrine, and forbidden words are **deterministic per day** — same state
  for all conversations on a given day, changes at midnight.
- `validate_with_oracle()` is **deterministic per input + date** — the same
  approach gets the same verdict all day, but may change tomorrow.
- Resources are not auto-fetched by most clients; the `instructions` in the
  server are what reliably drive LLM behavior.
