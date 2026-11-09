# The Albuquerque Files

An original, retro-modern geography detective game. Episode 01: **The Missing Sky**.

## Play locally

No build step or dependencies are required. Serve the `dist` directory:

```sh
python3 -m http.server 8080 --directory dist
```

Open http://localhost:8080. Progress saves in browser localStorage.

## Gameplay

Follow witness clues from London through Lisbon and Cairo to Jaipur. Investigations and flights advance the 72-hour clock. Collect identifying evidence, match a suspect dossier, request a warrant, confirm the courier's final location, and make an arrest. Wrong destinations consume time but allow recovery. Includes success, wrong-arrest, and timeout endings and case restart.

## Structure

- `dist/index.html` — accessible application shell
- `dist/style.css` — responsive terminal-inspired visual design
- `dist/game.js` — case data, original SVG city illustrations, state and interactions
- `.openai/hosting.json` — private Sites deployment configuration

All illustrations and narrative were created for this game. Travel times are simplified game mechanics. This is the first complete case, not yet a multi-case campaign.
