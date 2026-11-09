# The Albuquerque Files

A retro-modern geography detective game. The current prototype is an explorable London district for **The Missing Sky**.

## Run

No dependencies or build step:

```sh
python3 -m http.server 8080 --directory dist
```

Open http://localhost:8080.

## Play

- Move with WASD or arrow keys, or click/tap the ground. Tap routes navigate around buildings and the fountain.
- Approach a witness or searchable object and press E, or use the contextual interaction button. Nearby characters can also be clicked/tapped.
- Press N or select Notebook to review automatically recorded evidence.
- Question the guard, inspect the packing crate, speak to the café owner, and search near the fountain. Use your evidence to answer the travel clerk's geography question.
- Movement is free. Each new clue costs two case hours. Wrong answers provide feedback and allow another attempt.
- The prototype ends with the correct London deduction; Lisbon exploration is not implemented yet. You can continue exploring London afterward.
- Progress saves in browser localStorage, separately from the original case. Original dashboard files remain at `classic.html` for development reference.

## Files

`dist/explore.js` contains original canvas art, animation, collision, tap pathfinding, dialogue, clues, notebook, and persistent state. `dist/explore.css` handles responsive presentation; `dist/index.html` is the minimal game shell. `.openai/hosting.json` identifies the existing private Sites deployment.
