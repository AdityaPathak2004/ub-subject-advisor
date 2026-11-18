# UB Subject Advisor (unofficial demo)

A lightweight web app that helps prospective University at Buffalo students find a major.
Students upload their previous results, pick their interests and get a research-paper-style
report ranking UB undergraduate programs, with step-by-step reasoning and an AI chatbot.

**Live site:** https://adityapathak2004.github.io/ub-subject-advisor/

## Features
- Upload results as CSV/JSON (percentages, letter grades, GPA, SAT), or load the demo student
- Interest picker, career goal and applicant type
- Scoring model: 60% academic fit, 30% interests, 10% career goal
- Gemini AI reasons through the evidence step by step, with a built-in engine as offline fallback
- "Ask the advisor" chatbot that streams Gemini replies, with built-in answers when AI is off
- Report styled like a research paper (abstract, tables, figure, discussion, references), printable to PDF
- Session restore, undo, toasts, back-to-top, keyboard access, mobile layout

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
