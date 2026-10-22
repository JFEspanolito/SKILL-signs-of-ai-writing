# writing-pattern-audit

An agent skill that audits and edits text using the 101 rules derived from [Wikipedia:Signs of AI writing (WP:AISIGNS)](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by Wikipedia's [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup).

The guide targets ChatGPT, Claude, Gemini, Grok, DeepSeek, and other language models. Its objective is to produce accurate, specific, and natural writing while avoiding repetitive stylistic patterns associated with AI-generated content.

## Installation

```bash
npx skills@latest add JFEspanolito/SKILL-signs-of-ai-writing
```

## Scope tags

Rules in [`SKILL.md`](skills/writing-pattern-audit/SKILL.md) apply universally unless marked with a scope tag:

- `[W]` applies only to Wikipedia (MediaWiki, wikitext, templates, and Wikipedia policies).
- `[C]` applies to comments, pull requests, edit summaries, change logs, GitHub, technical documentation, and content management systems.

## What it detects

The 101 rules are organized into eight sections:

1. Content, accuracy, and depth (Rules 1–18): exaggerated significance, artificial legacy statements, vague associations ("related to", "connected to"), invented consensus, fabricated ecological connections, and promotional adjectives.
2. Language, vocabulary, and sentence construction (Rules 19–37): overused vocabulary separated by model era (mid-2025 to mid-2026 GPT-5 era vs. mid-2026 onward GPT-6 era), negative parallelism ("Not only X, but also Y"), forced rule-of-three lists, false ranges ("from X to Y"), interpretive participial phrases, and uniform sentence lengths.
3. Formatting and visual structure (Rules 38–51): Markdown in plain-text destinations, systematic `- **Bold:** explanation` lists, unnecessary tables, title case in headings, empty headings, and decorative emojis.
4. Communication and conversational behavior (Rules 52–65): automatic introductions ("Certainly!", "Here's a detailed breakdown"), unresolved placeholders, generic disclaimers about source availability, didactic disclaimers on how sources should be interpreted, and knowledge-cutoff notes.
5. Sources, references, and verification (Rules 66–77): fabricated citations or identifiers (DOIs, ISBNs, PMIDs), AI tracking parameters (`utm_source=chatgpt.com`, `utm_source=openai`, `referrer=grok.com`), and internal citation artifacts (`oaicite`, `turn0search0`, `[cite: 1]`, `grok_card`, `【85†L261-269】`).
6. Comments, publications, and change logs (Rules 78–90): customer-service phrasing in comments, self-promotional edit summaries ("Significantly improved clarity, coherence, neutrality, and overall quality"), unverified compliance guarantees, and abrupt shifts in an existing author's voice.
7. Additional rules derived from historical indicators (Rules 91–95): patterns from earlier model generations, including template "In Conclusion" sections, synonym cycling for lexical diversity, and reused bibliographic access dates.
8. Quality rules that must not be confused with AI indicators (Rules 96–101): guards against introducing deliberate typos, sacrificing technical precision for informality, deleting valid citations, banning individual words out of context, or hiding substantive errors behind cosmetic edits.

## Audit priorities

Vocabulary lists (Rules 19–20) are a secondary signal because marker words change with every model generation. When auditing a text, the skill checks the five signs that the publication identifies as most common in newly generated text (as of October 2026) first:

1. Markdown presence where the destination does not use it (Rule 49).
2. AI-style edit summaries and change logs (Rules 82–87).
3. Hedging disclaimers about source availability (Rule 58) and disclaimers about how sources should be used or interpreted (Rule 59).
4. Vague expressions of connection or association (Rules 9–10).
5. Canned emphasis on notability, source attribution, and media coverage (Rules 4, 11–13).

After checking those five signs, the skill works through the sections in this operational order:

1. Factual accuracy and traceability: correct information, verifiable references, and explicit relationships.
2. Communication precision: concrete ideas, proportional explanations, and no interpretive filler.
3. Natural editorial style: appropriate vocabulary, varied sentence construction, and minimal formulaic repetition.
4. Destination-compatible formatting: no internal artifacts, incompatible markup, or unnecessary structures.

## Usage examples

Once installed, invoke the skill in your agent prompt when drafting or reviewing text:

```text
Audit this README with writing-pattern-audit and fix any structural or formatting issues.
```

```text
Review my pull request description and commit log using the [C] rules in writing-pattern-audit.
```

```text
Edit docs/architecture.md with writing-pattern-audit to replace vague associations, negative parallelisms, and promotional adjectives while preserving the technical facts.
```

## License

[MIT](LICENSE) © 2026 JFEspanolito
