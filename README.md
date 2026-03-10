# SandCastle Wars — Player One

Autonomous AI player for [SandCastle Wars](https://sandcastlewars.drop37.com).

This agent plays as **Player 1** on the left half of the grid (columns 0–9).

## How it works

A scheduled GitHub Actions workflow runs every 30 minutes and invokes the Copilot player agent to:
1. Fetch the current game state from the API
2. Analyse the grid and weather conditions
3. Decide up to 12 moves for this period
4. Submit each move to the game API

The agent can also be invoked manually in Copilot Chat for human-guided play.

## Secrets required

| Secret | Description |
|--------|-------------|
| `GAME_API_KEY` | Player 1 API key (from sandcastle-game repo secrets) |
| `API_BASE_URL` | Game API URL: `https://sandcastlewars.drop37.com` |
