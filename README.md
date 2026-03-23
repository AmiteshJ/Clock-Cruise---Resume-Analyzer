# Resume Analyzer

A simple web app that analyzes resume text and returns extracted skills, a suggested job role, and a score out of 100.

Built as a technical assessment for an internship application.

---

## Live Demo

[Click here to view the app](#) ← replace with your Netlify link

---

## Features

- Paste resume text and click Analyze
- Detects skills across 6 categories (Frontend, Backend, Database, DevOps, Data Science, Mobile)
- Suggests a job role based on detected skills
- Scores the resume from 0 to 100
- AI-powered feedback via Anthropic Claude API

---

## Tech Stack

- HTML, CSS, JavaScript (vanilla — no frameworks)
- Anthropic Claude API for AI feedback

---

## How to Run

No installation needed.

Just download `resume-analyzer.html` and open it in any browser.

---

## How the Score is Calculated

| Signal | Points |
|---|---|
| Each detected skill | 3 pts (max 25) |
| Resume longer than 100 words | 8 pts |
| Resume longer than 250 words | 7 pts |
| Resume longer than 450 words | 5 pts |
| Standard sections (Experience, Education, etc.) | 4 pts each |
| Email present | 5 pts |
| Phone number present | 3 pts |
| GitHub / LinkedIn URL | 3 pts each |

Max score: 100

---

## Project Structure

Single file project — all HTML, CSS, and JS is in `resume-analyzer.html`.

The logic is split into clearly commented functions:

- `extractSkills()` — keyword matching across 6 skill categories
- `suggestRole()` — rule-based role suggestion from detected skills
- `scoreResume()` — computes score from multiple resume signals
- `fetchAIFeedback()` — calls Anthropic API for personalized feedback
