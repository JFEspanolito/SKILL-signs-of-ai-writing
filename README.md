# writing-pattern-audit

An agent skill that audits and edits text against 101 concrete rules derived from [Wikipedia:Signs of AI writing (WP:AISIGNS)](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). It focuses on structural accuracy, source verifiability, and natural prose rather than superficial word-swap tricks.

## Installation

```bash
npx skills@latest add JFEspanolito/SKILL-signs-of-ai-writing
```

## Scope tags

Rules in `SKILL.md` are universal unless marked with a scope tag:

1. `[W]` Wikipedia-specific (MediaWiki, wikitext, templates, Wikipedia policies). Ignored outside Wikipedia.
2. `[C]` Comments, pull requests, edit summaries, and change logs. Applies to GitHub, technical documentation, and content management systems.

## What it detects

Rather than treating AI writing as a simple list of banned words, the skill checks eight structural and stylistic categories across 101 numbered rules:

1. Content, accuracy, and depth (Rules 1–18): inflated significance, artificial legacy statements, vague associations ("related to", "connected to"), invented consensus, and promotional adjectives.
2. Language, vocabulary, and sentence construction (Rules 19–37): generation-specific marker clusters (GPT-5 and GPT-6 eras), repetitive negative parallelism ("Not only X, but also Y"), forced rule-of-three lists, false ranges ("from X to Y"), and uniform sentence lengths.
3. Formatting and visual structure (Rules 38–51): Markdown in plain-text destinations, systematic `- **Bold:** explanation` lists, title case in headings, and decorative emojis.
4. Communication and conversational behavior (Rules 52–65): chatbot preambles ("Certainly!", "Here's a breakdown"), hedging disclaimers on source availability, didactic notes on how to interpret sources, and leftover placeholders.
5. Sources, references, and verification (Rules 66–77): fabricated citations or DOIs, AI tracking parameters (`utm_source=chatgpt.com`), and internal citation artifacts (`oaicite`, `turn0search0`, `[cite: 1]`).
6. Comments, publications, and change logs (Rules 78–90): customer-service phrasing in technical reviews, self-promotional edit summaries ("Significantly improved clarity and coherence"), and unverified compliance claims.
7. Additional rules derived from historical indicators (Rules 91–95): knowledge-cutoff notices, template "In Conclusion" sections, and aggressive synonym cycling.
8. Quality rules that must not be confused with AI indicators (Rules 96–101): prevents over-corrections such as deleting valid citations, introducing fake typos, or hiding factual errors behind cosmetic rewrites.

## Audit priorities

Vocabulary lists age with every model release. When auditing a text, the skill first checks the five patterns that Wikipedia's guide identifies as the most common signs in newly generated text (as of October 2026):

1. Markdown syntax in destinations that do not use it (Rule 49).
2. AI-style edit summaries and change logs (Rules 82–87).
3. Hedging disclaimers about source availability (Rule 58) and didactic notes on how sources should be used or interpreted (Rule 59).
4. Vague expressions of connection or association where concrete facts exist (Rules 9–10).
5. Canned emphasis on notability, source attribution, and media coverage (Rules 4, 11–13).

After checking those five indicators, the audit follows a strict four-step operational order:

1. Factual accuracy and traceability: verify claims, citations, and explicit relationships.
2. Communication precision: cut interpretive filler and unsupported extrapolations.
3. Natural editorial style: vary sentence rhythm and remove formulaic transitions.
4. Destination-compatible formatting: strip internal model tokens and match the target platform's markup.

## Usage examples

Once installed, your coding agent loads the skill automatically when you ask for an editorial pass or writing audit:

```text
Audit this README with writing-pattern-audit and fix any structural or formatting issues.
```

```text
Review my pull request description and commit log using the [C] rules in writing-pattern-audit.
```

```text
Edit docs/architecture.md to remove vague associations, negative parallelisms, and promotional filler while keeping the technical claims intact.
```

## Sources

- [Wikipedia:Signs of AI writing (WP:AISIGNS)](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by Wikipedia's [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup).
- Repository layout convention adapted from [Emil Kowalski's skill repository structure](https://github.com/emilkowalski).

## License

MIT © 2026 JFEspanolito
