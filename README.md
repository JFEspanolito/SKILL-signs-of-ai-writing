# writing-pattern-audit

An open-source Agent Skill that audits and improves writing using 101 editorial rules adapted from [Wikipedia:Signs of AI writing (WP:AISIGNS)](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by Wikipedia's [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup).

This project reorganizes and paraphrases the source material into actionable instructions for AI agents. It does not claim original authorship of the underlying research, observations, or writing patterns.

The skill can be used with ChatGPT, Claude, Gemini, Grok, DeepSeek, and other compatible AI agents to identify formulaic language, structural weaknesses, unsupported claims, and formatting issues.

Its purpose is to improve accuracy, clarity, specificity, and natural writing, not to guarantee that AI-generated text will be undetectable.

## Installation

Install using [Skills CLI](https://skills.sh/):

```bash
npx skills@latest add JFEspanolito/SKILL-signs-of-ai-writing
```

The skill can be installed globally or within individual projects, depending on the agent and installation options.

## Recommended execution

The following prompt performs a non-destructive audit of an entire project and generates a Markdown report at `AI/request/reviews/writing_audit.md`.

The agent must report proposed corrections without modifying the original content, allowing you to review each finding before making changes.

````markdown
Use the installed `writing-pattern-audit` skill to perform a comprehensive writing audit of the entire project.

**Objective:** Identify writing patterns associated with AI-generated content, structural weaknesses, unsupported claims, repetitive language, and opportunities to improve clarity, accuracy, and naturalness across all user-facing content.

### Instructions

1. **Load the skill first**
   - Locate and load the installed `writing-pattern-audit` skill using the agent's skill discovery mechanism.
   - Read its `SKILL.md` before starting the audit.
   - Follow its rules, audit priorities, severity classifications, and context-specific exceptions.
   - Do not substitute the skill with a generic editorial review.

2. **Audit the entire project**
   - Inspect all relevant user-facing text, including website pages, UI components, headings, descriptions, metadata, documentation, and other content intended for readers.
   - Include text embedded in source files, configuration files, and content collections.
   - Exclude generated files, dependencies, build outputs, unrelated program logic, and the designated audit report.
   - Preserve technical terminology, product names, and established domain-specific vocabulary.

3. **Identify and classify findings**
   - Apply the skill's P0–P3 severity classifications.
   - Prioritize factual inaccuracies, unsupported claims, and relevant structural patterns.
   - Identify repetitive AI-style phrasing, artificial transitions, vague claims, promotional filler, false ranges, unnecessary disclaimers, and unnatural sentence structures.
   - Avoid false positives. Do not flag valid Markdown, legitimate technical language, or appropriate stylistic choices simply because they resemble AI-generated patterns.
   - Distinguish confirmed issues from subjective stylistic recommendations.
   - Apply Wikipedia-specific checks only when the destination is Wikipedia or MediaWiki.

4. **Generate the audit report**

   Create or update:

   `AI/request/reviews/writing_audit.md`

   Include:
   - Executive summary.
   - Audit scope and methodology.
   - Total files reviewed.
   - Total findings by priority (P0, P1, P2, P3).
   - Findings grouped by file.
   - Relevant skill rule IDs for each finding.
   - A complete correction table.

   Use this format:

   | Priority | Rule | File | Line | Actual Text | Recommended Text | Reason |
   |---|---|---|---|---|---|---|

5. **Correction requirements**
   - Quote the exact original text as it appears in the project.
   - Provide a complete, ready-to-use replacement for each finding when the evidence supports one.
   - Preserve the original meaning, factual claims, and intended tone.
   - Do not invent facts, statistics, citations, or supporting evidence.
   - If a claim cannot be verified, flag it for verification rather than inventing a replacement.
   - Do not recommend superficial synonym substitutions that fail to improve the writing.
   - Avoid duplicate findings for the same underlying issue.

6. **Coverage and traceability**
   - Use repository-relative file paths and accurate line numbers wherever possible.
   - Make every finding traceable to its source.
   - Report files that were skipped and explain why.
   - If a file contains no findings, include it in the audit coverage summary rather than inventing issues.
   - Do not claim complete coverage unless all relevant files were inspected.

### Constraints

- Do not modify any existing project files except the designated audit report.
- Do not automatically apply corrections to audited content.
- Do not create commits, branches, or pull requests.
- Only create or update `AI/request/reviews/writing_audit.md`.
- Create the parent directories if they do not exist.
- Do not request confirmation for each finding; complete the audit and produce the report.
- Do not claim that any text was definitively generated by AI. Report observable writing patterns and quality issues instead.

### Expected result

A comprehensive, actionable Markdown audit that allows me to review every proposed change before deciding whether to implement it.

Prioritize substantive quality problems over cosmetic changes and provide exact original-to-recommended text comparisons.
````

## Scope tags

Rules in [`SKILL.md`](skills/writing-pattern-audit/SKILL.md) apply generally unless marked with a scope tag:

- `[W]` — Wikipedia-specific rules covering MediaWiki, wikitext, templates, and Wikipedia policies.
- `[C]` — Rules applicable to comments, pull requests, edit summaries, change logs, GitHub, technical documentation, and content management systems.

Context matters. A writing pattern should not be treated as an error simply because it resembles a known AI-generated construction.

## What it detects

The 101 rules are organized into eight sections:

1. Content, accuracy, and depth (Rules 1–18): Exaggerated significance, artificial legacy statements, vague associations, invented consensus, fabricated ecological connections, and promotional adjectives.
2. Language, vocabulary, and sentence construction (Rules 19–37): Model-era vocabulary patterns, negative parallelism, forced rule-of-three lists, false ranges, interpretive participial phrases, and uniform sentence lengths.
3. Formatting and visual structure (Rules 38–51): Incompatible Markdown, repetitive bold-label lists, unnecessary tables, excessive heading capitalization, empty headings, and decorative emojis.
4. Communication and conversational behavior (Rules 52–65): Automatic introductions, unresolved placeholders, generic disclaimers, unnecessary source-interpretation warnings, and knowledge-cutoff notices.
5. Sources, references, and verification (Rules 66–77): Fabricated citations, invalid identifiers, AI tracking parameters, and internal citation artifacts.
6. Comments, publications, and change logs (Rules 78–90): Customer-service phrasing, self-promotional edit summaries, unsupported compliance claims, and abrupt changes in an author's voice.
7. Historical indicators (Rules 91–95): Patterns associated with earlier model generations, including formulaic conclusions, excessive synonym cycling, and reused bibliographic access dates.
8. Quality safeguards (Rules 96–101): Preventing artificial mistakes, loss of technical precision, removal of valid citations, indiscriminate word bans, and cosmetic changes that conceal substantive problems.

## Audit priorities

The skill distinguishes between current high-frequency indicators, substantive writing problems, and historical stylistic patterns.

According to the source publication's October 2026 guidance, five particularly common indicators in newly generated Wikipedia content are:

1. Markdown syntax in destinations where it is not appropriate (Rule 49).
2. AI-style edit summaries and change logs (Rules 82–87).
3. Hedging disclaimers about source availability (Rule 58) and didactic notes on how sources should be used or interpreted (Rule 59).
4. Vague expressions of connection or association (Rules 9–10).
5. Formulaic emphasis on notability, source attribution, and media coverage (Rules 4, 11–13).

These indicators are context-dependent and should not be treated as universal proof of AI authorship.

### Operational order

1. Factual accuracy and traceability: Correct information, verifiable references, and explicit relationships.
2. Communication precision: Concrete ideas, proportional explanations, and minimal interpretive filler.
3. Natural editorial style: Appropriate vocabulary, varied sentence construction, and minimal formulaic repetition.
4. Destination-compatible formatting: No internal artifacts, incompatible markup, or unnecessary structures.

### Finding severity

| Priority | Severity | Description |
|---|---|---|
| P0 | Critical | Factual inaccuracies, fabricated references, misleading claims, and serious source-integrity problems. |
| P1 | High | Significant structural problems, unsupported significance claims, vague associations, and applicable high-frequency indicators. |
| P2 | Medium | Formulaic language, repetitive constructions, unnecessary transitions, unnatural phrasing, and clarity issues. |
| P3 | Low | Minor stylistic inconsistencies, historical indicators, and optional cosmetic improvements. |

Each finding should identify the applicable rule, its severity, the original text, the proposed correction, and the reasoning behind the recommendation.

## Usage examples

Audit a README:

```text
Audit this README with writing-pattern-audit and identify structural or formatting issues. Do not modify the file.
```

Review a pull request:

```text
Review my pull request description and commit log using the [C] rules in writing-pattern-audit.
```

Improve technical documentation:

```text
Use writing-pattern-audit to review docs/architecture.md for vague associations, negative parallelism, and promotional language while preserving technical accuracy.
```

Review a single paragraph:

```text
Use writing-pattern-audit to identify AI-style writing patterns in this paragraph and propose a more natural version without changing its meaning.
```

## Source and attribution

This skill is adapted from:

**Wikipedia contributors. [Wikipedia:Signs of AI writing (WP:AISIGNS)](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).** Maintained through [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup).

The source material is available under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

For the original contributors and revision history, see the [Wikipedia page history](https://en.wikipedia.org/w/index.php?title=Wikipedia:Signs_of_AI_writing&action=history).

### Adaptations made

The original material has been:

- Paraphrased and reorganized into 101 actionable writing rules.
- Structured for use by AI coding and writing agents.
- Grouped by writing category and application context.
- Supplemented with audit priorities, severity classifications, and execution instructions.
- Reformatted as an installable Agent Skill.

This project is an independent adaptation and is not affiliated with, endorsed by, or maintained by Wikipedia, the Wikimedia Foundation, or WikiProject AI Cleanup.

## License

The adapted skill content is distributed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

You are free to:

- Share: Copy and redistribute the material in any medium or format.
- Adapt: Remix, transform, and build upon the material for any purpose, including commercially.
- Use: Install and run the skill with compatible AI agents.

When redistributing or adapting the material, you must provide appropriate attribution, link to the license, indicate whether changes were made, and distribute adaptations under the same license or a compatible license.

See the [`LICENSE`](LICENSE) file for licensing details.