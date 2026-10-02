# Raise_project
Opportunity: Help Parents Build a Friendly, Trust-Based Relationship with Their Teens, Raise helps parents balance guidance with empathy, building open communication and trust so teens feel comfortable turning to them for advice and support.

---

Raise helps parents prepare for difficult conversations with their teenager, have them offline, reflect, and plan the next one.

Live prototype: https://shuklahimanshu20.github.io/Raise_project/

## Flow
Cover → Get started → Log in (username + password) / Create a parent account / Forgot password
→ Teen's age group → Topic → Hardest part → 5-minute guide written by Raise AI (Understand, Start, Anticipate, Avoid, Ready)
→ Customize with AI: chat about your teen and add tailored openers and tips to the guide
→ Go talk (pocket card) → Reflect (went well / stalled / unexpected) → Insight + next conversation → Home & Journal

## Raise AI (simulated)
Tapping **Build my 5-minute guide with AI** and **Customize with AI** opens a chat where the parent describes their teen (shy, uses Snapchat, walks off when topics come up, wants a 1-minute version, and so on). Raise AI replies with coaching plus a suggested opener or tip that can be added to the guide and the pocket card in one tap.

In this prototype the AI is simulated: replies come from a rules-based engine in `project/Main.dc.html` (`aiReply`), so it runs on GitHub Pages without an API key or cost. A production version would send the same context (topic, age group, difficulty, teen description) to an LLM through a backend that keeps the API key private.

## Files (`project/`)
- `Main.dc.html` — the full interactive prototype (all screens, content and logic)
- `Login`, `Signup`, `Prep`, `Chat`, `Talk`, `Reflect`, `Insight`, `Home` `.dc.html` — frames that open the prototype at that screen with sample data
- `canvas.json` — canvas layout

`index.html` renders `project/Main.dc.html` in the browser with React. To run locally, serve the folder (for example `python -m http.server`) and open http://localhost:8000. Jump to a screen with `?screen=home&demo=1` or `?screen=prep&step=2&demo=1`.
