# Match Terminal for Claude

Football results, match statistics and pre-match metric breakdowns from [Match Terminal](https://matchterminal.org).

Connects to the hosted, read-only MCP server at `https://mcp.matchterminal.org/mcp`. No API key or account is needed.

## Install

```
/plugin marketplace add rkivi/match-terminal-claude
/plugin install match-terminal@match-terminal
```

## Tools

| Tool | What it does |
| --- | --- |
| `search_matches` | Find fixtures and results by team, opponent, date, competition or status. |
| `get_match_statistics` | Result, team statistics, events and timestamps for a match. |
| `get_team_ratings` | 30 rolling pre-match metrics and five group ratings for both teams. |

## Example prompts

- Show yesterday's results for Arsenal.
- Show match statistics for Fiji vs New Caledonia.
- Compare strength, scoring, control, passing and defence for [team] vs [opponent].

## What this plugin sends and runs

- It runs no local code, scripts or hooks. It only adds one remote MCP server and one skill.
- When Claude calls a tool, it sends the tool arguments (team names, opponent, date, competition or status filter, result limit, or a selected match ID) to `https://mcp.matchterminal.org/mcp` over HTTPS. Nothing else from your conversation is sent.
- The server reads Match Terminal's own football database and returns match data. It does not store your tool arguments or chat history.
- The match card shows a link to the match page on matchterminal.org. Opening it is a normal website visit.

## Privacy Policy

Match Terminal's privacy policy covers this plugin: https://matchterminal.org/privacy. It explains what data is collected, how it is used and stored, which service providers process it, how long it is kept, and how to contact us.

## Notes

- Coverage varies by competition. Missing values are reported, never invented.
- Not betting advice. Player ratings are currently unavailable.
- [Terms](https://matchterminal.org/terms) · [Support](https://matchterminal.org/contact) · contact@matchterminal.org
