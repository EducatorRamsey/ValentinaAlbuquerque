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

## Turn-based apprehension prototype

After identifying Lisbon, speak to the travel clerk to confront Albuquerque's lookout. Existing completed London saves can start the encounter the same way. Four contextual actions appear only during the encounter: Restrain, Evade, Use evidence, and Talk down. Intent cues explain the next move. Restrain succeeds at resolve 2 or lower; reducing resolve to zero causes surrender. Physical evidence is stronger than testimony and each clue can be used once per attempt. Evading a rush lowers resolve and restores stamina. Failure after five turns or zero stamina costs three case hours and allows a retry. Progress and used evidence persist across reloads. Escape pauses the encounter; return to the clerk to resume. Successful apprehension adds the statement to the notebook.
