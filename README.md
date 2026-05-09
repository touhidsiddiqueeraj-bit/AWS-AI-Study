# AWS AI Practitioner Study App — AIF-C01

A self-contained, single-file HTML study app for the **AWS Certified AI Practitioner (AIF-C01)** exam. No install, no backend, no dependencies — open the file in any browser and start studying.

---

## Features

- **20-day structured study plan** aligned to all 5 official exam domains
- **7 practice test sets** — 105 questions with immediate feedback and explanations
- **Notes / cheat sheet tab** covering every in-scope service and concept
- **XP & levelling system** to keep motivation up
- **Streak tracking** with daily activity heatmap
- **Dark and light mode**
- **Keyboard shortcuts** (1–4) for answering quiz questions
- **Progress saved locally** — `localStorage`, no account needed
- Fully responsive — works on desktop and mobile

---

## Study Plan Overview

| Phase | Days | Focus |
|---|---|---|
| Week 1 | 1–7 | AI/ML fundamentals, supervised vs unsupervised, neural networks, evaluation metrics, GenAI & Transformers |
| Week 2 | 8–14 | AWS AI stack — Bedrock, SageMaker, Amazon Q, Rekognition, Comprehend, HealthScribe, Responsible AI |
| Week 3 | 15–19 | Prompt engineering, Bedrock Agents & Knowledge Bases, FM customisation, security, compliance & governance |
| Final | 20 | Full review across all 5 domains |

---

## Exam Domains Covered

| Domain | Weight | Coverage |
|---|---|---|
| 1 — Fundamentals of AI and ML | 20% | Days 1–7, Sets 1–2 |
| 2 — Fundamentals of GenAI | 24% | Days 5–7, Sets 3–4 |
| 3 — Applications of Foundation Models | 28% | Days 15–17, Set 6 |
| 4 — Guidelines for Responsible AI | 14% | Days 13–14, Set 5 |
| 5 — Security, Compliance & Governance | 14% | Days 18–19, Set 7 |

---

## Usage

```
# Just open it
open aws-ai-practitioner-study.html
```

No build step. No server. No npm. Drop the file anywhere and open it in Chrome, Firefox, Safari, or Edge.

To host it (optional):

```bash
# GitHub Pages — put the file in your repo root, enable Pages, done.
# Or any static host: Netlify, Vercel, Cloudflare Pages.
```

---

## What's Inside

```
aws-ai-practitioner-study.html   ← the entire app, one file
README.md
```

All study data — days, checklists, questions, notes — lives in plain JavaScript arrays inside the HTML. Easy to read and edit directly.

**To add or edit content**, open the file in any text editor and find:

- `var DAYS = [...]` — study day topics, checklists, focus questions, key terms
- `var ALL_TESTS = [...]` — practice questions, options, answers, explanations
- `var NOTES_REF = [...]` — cheat sheet entries by section
- `var PHASES = [...]` — phase labels and day ranges

---

## Practice Tests

| Set | Topic |
|---|---|
| Set 1 | AI & ML Fundamentals |
| Set 2 | AWS AI Services |
| Set 3 | Generative AI & Foundation Models |
| Set 4 | Responsible AI & Governance |
| Set 5 | Mixed Exam Simulation |
| Set 6 | Prompt Engineering & FM Applications (Domain 3) |
| Set 7 | Security, Compliance & Governance (Domain 5) |

Answer positions are randomised across A/B/C/D — no answer-pattern shortcuts.

---

## Exam Quick Reference

- **Format:** 65 questions (50 scored + 15 unscored), ~90 minutes
- **Passing score:** 700 / 1000
- **Question types:** multiple choice, multiple response, ordering, matching
- **Recommended experience:** up to 6 months exposure to AWS AI/ML services
- **Official guide:** [AIF-C01 Exam Guide (PDF)](https://docs.aws.amazon.com/pdfs/aws-certification/latest/ai-practitioner-01/ai-practitioner-01.pdf)

---

## Key Services to Know

**Core AI services:** Amazon Bedrock, Amazon SageMaker AI, Amazon Q Developer, Amazon Q Business

**Pre-built AI:** Rekognition, Comprehend, Comprehend Medical, Transcribe, Polly, Translate, Kendra, Lex, HealthScribe

**Bedrock features:** Agents, Knowledge Bases, Guardrails, Model Evaluation, Prompt Management

**SageMaker tools:** Studio, Ground Truth, Canvas, Clarify, Model Monitor, Data Wrangler, Feature Store, Model Cards, JumpStart

**Governance:** CloudTrail, AWS Config, Audit Manager, Artifact, Inspector, Macie, A2I, PrivateLink

---

## Local Storage Keys

Progress is saved automatically to `localStorage` under these keys:

| Key | Contents |
|---|---|
| `awsai_done` | Completed day numbers |
| `awsai_subs` | Checklist item states |
| `awsai_xp` | Total XP earned |
| `awsai_scores` | Test set scores |
| `awsai_dates` | Study dates (for streak) |
| `awsai_lightmode` | Theme preference |

To reset all progress: open DevTools → Application → Local Storage → clear all `awsai_*` keys.

---

## Contributing

Content corrections and new questions are welcome. The data format for a question is:

```js
{
  q: "Question text?",
  opts: ["Option A", "Option B", "Option C", "Option D"],
  ans: 2,   // 0-indexed correct answer
  exp: "Explanation shown after answering."
}
```

Please vary the `ans` index when adding questions — avoid making every correct answer the same position.

---

## License

MIT — use freely, study hard, pass the exam.
