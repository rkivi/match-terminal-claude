---
name: football-data
description: Look up football (soccer) fixtures, results, match statistics and pre-match metrics from Match Terminal. Use when the user asks about a football match, team results, scores, match stats, or comparing two teams before a match.
---

# Match Terminal football data

Use the `match-terminal` MCP tools. All data is read-only and comes from the Match Terminal cache.

## Finding a match

- Search by team names with `search_matches`, adding an opponent and/or UTC date (`YYYY-MM-DD`) when the user gives them. Never ask the user for a match ID.
- Without a date, team searches return the latest cached matches across dates. Without a team or date, the search defaults to today (UTC).
- Show the returned numbered list with full team names, competition, country and kickoff. Wait for the user to pick one. Never pick the first or only result automatically.
- If results are truncated, offer to narrow by fuller team name, opponent or date.

## Getting details

- `get_match_statistics`: result, team statistics, events and timestamps for the selected match. Where the client shows the Match Terminal card, it also includes available pre-match context.
- `get_team_ratings`: pre-match breakdown — 30 rolling prior-match metrics and five group ratings (strength, scoring, control, passing, defence) with input coverage.

## Rules

- Keep returned units, match windows, zero values, missing values, source and calculation timestamps.
- Pre-match metrics describe earlier matches, not performance in the selected fixture.
- Say clearly when data is missing. Never invent values.
- Do not give betting advice or guarantee outcomes.
- Player ratings are not available. Do not offer or infer them.
