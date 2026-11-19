# UB Subject Advisor (unofficial demo)

A lightweight web app that helps prospective University at Buffalo students find a major.
Students upload their previous results, pick their interests and get a research-paper-style
report ranking UB undergraduate programs, with step-by-step reasoning and an AI chatbot.

**Live site:** https://adityapathak2004.github.io/ub-subject-advisor/

## Features
**Core**
- Upload results as CSV/JSON (percentages, letter grades, GPA, SAT), or load the demo student
- Scoring model (60% academic fit, 30% interests, 10% goal) + Gemini step-by-step reasoning, with offline fallback
- Research-paper-style report (abstract, tables, figure, discussion, references), printable to PDF
- "Ask the advisor" chatbot (streaming Gemini, voice input, knows your report and 4-year plan)

**Academic Advisor tab**
- Readiness scorecard per key subject · math-placement recommendation
- Interactive advising checklist (saved) · 4-week prep plans for weak subjects
- Questions to ask your advisor (+ AI advisor notes) · career paths · suggested minors

**4-Year Plan tab**
- 8-semester plan for all 18 programs with prerequisites in order and ~15 credits/term
- Move courses between semesters with a live prerequisite and credit-load checker
- Pick gen-ed courses · lighter first semester · start-with-Precalculus option
- 120-credit tracker · GPA planner · AI plan review with per-semester tips · CSV export

**More**
- Compare up to 3 programs side by side · What-if simulator (sliders)
- Program explorer with search/filter · 1-minute interest quiz
- Saved profiles · share link that reopens the exact report
- Dark mode · text size · keyboard shortcuts (press `?`) · session restore, undo, toasts

## AI access
The Gemini API key is stored **only encrypted** (AES-256-GCM, PBKDF2-SHA256 with 250k iterations)
in `index.html`. It is unlocked with a code that is **not** in this repository: enter it under
**Unlock AI**, or open a private link ending in `#unlock=<code>`. Without the code, the site runs
in built-in mode.

## Run locally
```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Demo data
`demo_student_results.csv` is a sample transcript (Arjun Mehta, CBSE Class XII + SAT).

---
Unofficial student project. Not affiliated with or endorsed by the University at Buffalo.
UB name and logo belong to the University at Buffalo. Course numbers are illustrative; confirm in the UB catalog.
