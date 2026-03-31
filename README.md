# Odds-API.io

An [agent skill](https://agentskills.io/home) that queries Odds-API.io for sports, bookmakers, events, and betting odds.

## What it does

When a user wants betting odds from Odds-API.io, this skill:

- Lists sports and bookmakers
- Searches events to find the right event ID
- Fetches odds for a chosen event
- Supports a one-step matchup flow for search plus odds
- Includes a helper CLI and a concise API reference

## Installation

### As a skill

```bash
npx skills add https://github.com/diegopetrucci/odds-api-io --skill odds-api-io
```

### As a Claude Code plugin

```shell
/plugin marketplace add diegopetrucci/ai-agents-skills
/plugin install odds-api-io@diegopetrucci-claude-plugins
```

## Usage

Trigger the skill when the user wants Odds-API.io data:

- **Claude Code:** `/odds-api-io`
- Or say: "what are the odds for Inter vs Arsenal", "show bookmakers for this event", or "query Odds-API.io for value bets"

The bundled helper script can also be run directly:

```bash
python3 odds-api-io/scripts/odds_api.py sports
python3 odds-api-io/scripts/odds_api.py bookmakers
python3 odds-api-io/scripts/odds_api.py search --query "Inter vs Arsenal" --sport football
python3 odds-api-io/scripts/odds_api.py odds --event-id 123456 --bookmakers "Bet365,Unibet"
```

## More Skills Like This

Found this skill useful? Browse all my hand-crafted ones in the [AI Agents skills](https://github.com/diegopetrucci/ai-agents-skills) repo.

## License

MIT
