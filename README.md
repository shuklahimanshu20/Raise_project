# Raise_project
Opportunity: Help Parents Build a Friendly, Trust-Based Relationship with Their Teens, Raise helps parents balance guidance with empathy, building open communication and trust so teens feel comfortable turning to them for advice and support.

---

Raise helps parents prepare for difficult conversations with their teenager, have them offline, reflect, and plan the next one.

Live prototype: https://shuklahimanshu20.github.io/Raise_project/

## Flow
Cover → Get started → Log in (username + password) / Create a parent account / Forgot password
→ Teen's age group → Topic → Hardest part → 5-minute prep guide (Understand, Start, Anticipate, Avoid, Ready)
→ Go talk (pocket card) → Reflect (went well / stalled / unexpected) → Insight + next conversation → Home & Journal

## Files (`project/`)
- `Main.dc.html` — the full interactive prototype (all screens, content and logic)
- `Login`, `Signup`, `Prep`, `Talk`, `Reflect`, `Insight`, `Home` `.dc.html` — frames that open the prototype at that screen with sample data
- `canvas.json` — canvas layout

`index.html` renders `project/Main.dc.html` in the browser with React. To run locally, serve the folder (for example `python -m http.server`) and open http://localhost:8000. Jump to a screen with `?screen=home&demo=1` or `?screen=prep&step=2&demo=1`.
