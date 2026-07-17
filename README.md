# Hedi Tebourbi — a portfolio you can chat with

**Live at [redpill47.github.io](https://redpill47.github.io/)**

Instead of another scrolling CV page, this portfolio is styled as a chat
interface (a design homage to [Claude](https://claude.ai) by Anthropic):
you ask questions — or click a suggestion — and it answers about my research,
projects, publications, and experience.

Ask it *"Who is Hedi?"*, *"Show me his projects"*, or try something off-topic
and see what happens.

## What's inside

- **Research** — LLMs for low-resource languages (Luxembourgish), RAG
  evaluation, multi-agent systems, AI in education
- **6 peer-reviewed publications** (AAMAS, MobiSPC, MDPI, EUSPN, CALM, ACM CUI)
- **Featured projects** — ATLAS, LuxDiag Workbench, LuxDiag-RAG, KlangWee,
  and more
- Reviewer for AAMAS, MobiSPC, EUSPN, CALM, ArtInHCI

## How it works

One self-contained `index.html` — vanilla HTML/CSS/JS, no framework, no build
step, no backend. There's no LLM behind it either: every answer is hand-written
and keyword-matched, which makes this the only chat assistant with a
0% hallucination rate. Light/dark mode included.

Run it locally by opening `index.html`, or:

```sh
python -m http.server 8000
```

### Features & maintenance notes

- **Deep links** — `/#projects`, `/#publications`, `/#cv`, `/#p:atlas`
  (any topic or project id) opens the site with that answer already asked.
  Handy for email signatures and LinkedIn.
- **Per-project deep dives** — "tell me about ATLAS" (or KlangWee, the
  workbench, the homelab…) gets a dedicated detailed answer. Content lives in
  `PROJECT_DEEP` in `index.html`.
- **Availability** — the answer under `TOPICS.availability` currently says
  *not actively looking*. When that changes, rewrite that one answer.
- **CV download** — the `cv` topic links to `Hedi_Tebourbi_CV.pdf` in the repo
  root. Replace that file whenever the CV updates.
- **Analytics** — GoatCounter (privacy-friendly, no cookies), disabled by
  default. To enable: create a free site at [goatcounter.com](https://www.goatcounter.com),
  then set `const GOATCOUNTER = "yourcode"` near the bottom of `index.html`.
  Topic views are logged as `ask/<topic>` events and — the useful part —
  questions nobody could answer are logged as `unmatched/<question>`, which
  tells you what content to add next.
- **Link previews** — `og-image.png` is the card shown when the URL is shared
  on LinkedIn/WhatsApp/X; JSON-LD in the `<head>` describes the site for
  search engines.

## Contact

[LinkedIn](https://www.linkedin.com/in/hedit) ·
[GitHub](https://github.com/RedPill47) ·
[Google Scholar](https://scholar.google.com/citations?user=Tb6iPjcAAAAJ&hl=en) ·
[ORCID](https://orcid.org/0009-0006-1282-2820) ·
[X](https://x.com/Red_Pill_4)

---

*Design homage to Claude by Anthropic — not affiliated.*
