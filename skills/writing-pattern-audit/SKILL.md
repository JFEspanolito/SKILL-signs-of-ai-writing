---
name: writing-pattern-audit
description: "Trigger: AI writing audit, humanize text, remove AI patterns, editorial review, WP:AISIGNS. Audit and edit text using the 101 rules from Wikipedia's Signs of AI Writing."
license: CC-BY-SA-4.0
---

# Universal Rules for Avoiding AI-Generated Writing Patterns

Based on Wikipedia:Signs of AI Writing (WP:AISIGNS), these 101 rules establish writing standards applicable to ChatGPT, Claude, Gemini, Grok, DeepSeek, and other language models.

The original publication is a descriptive guide maintained by Wikipedia's WikiProject AI Cleanup, not an official Wikipedia policy. Some indicators are specific to Wikipedia, while others are associated with older generations of language models.

Objective: Produce accurate, natural, specific, and context-appropriate writing while avoiding repetitive stylistic patterns commonly associated with AI-generated content.

Avoiding these patterns does not guarantee that AI-generated text will be undetectable.

## Scope tags

Some rules only make sense in a specific destination. Untagged rules are universal.

- `[W]` Wikipedia-specific (MediaWiki, wikitext, templates, Wikipedia policies). Ignore outside Wikipedia.
- `[C]` Comments, pull requests, edit summaries, and change logs. Also applies to GitHub, technical documentation, and content management systems.

## Current priority (as of October 2026)

The publication states that the most common signs in newly generated text are the following five. Check these first, before any vocabulary list.

1. Markdown presence where the destination does not use it. See rule 49.
2. AI-style edit summaries and change logs. See rules 82 to 87.
3. Hedging disclaimers about source availability and source usage. See rules 58 and 59.
4. Vague expressions of connection or association. See rules 9 and 10.
5. Canned emphasis on notability, source attribution, and media coverage. See rules 4, 11, 12, and 13.

Vocabulary lists (rules 19 and 20) are a secondary signal. Marker words change with every model generation and are the easiest pattern to tune away, so a text can pass a word check and still fail on the five points above.

Do not treat these signs as the problems to fix. They are symptoms of deeper issues (unsupported claims, vague attribution, empty analysis). Fix the cause first. See rule 101.

## 1. Content, Accuracy, and Depth

1\. Avoid exaggerating the importance of a subject. Do not describe ordinary events as historic milestones, pivotal moments, or fundamental transformations without supporting evidence.

2\. Do not assign universal significance to local events. Avoid automatically connecting specific occurrences to broader social, cultural, or historical trends.

3\. Eliminate artificial legacy statements. Avoid phrases such as "left an indelible mark," "stands as a testament to," "marked a turning point," or "its legacy endures."

4\. Do not manufacture cultural significance. The existence of a tradition, company, person, or product does not automatically imply significant influence. Do not pad a subject with canned remarks about its media coverage or notability.

5\. Avoid superficial analysis. Statements such as "this reflects the importance of," "demonstrating its commitment to," or "highlighting its significance" require concrete supporting evidence.

6\. Do not add automatic interpretations. Avoid introducing symbolic, philosophical, or social explanations when the requested content is purely factual.

7\. Do not turn descriptions into advertisements. Avoid unjustified promotional enthusiasm when discussing people, products, companies, or places.

8\. Remove unnecessary promotional adjectives. Be cautious with words such as "vibrant," "innovative," "revolutionary," "exceptional," "prestigious," "iconic," "remarkable," and "renowned" unless they convey verifiable information.

9\. Describe relationships explicitly. Replace vague expressions such as "was associated with the company's leadership" with "was the company's director" when that is the verified fact.

10\. Avoid ambiguous associations. Do not use "related to," "associated with," "connected to," or "involved in" when the exact relationship can be identified.

11\. Do not invent consensus. Avoid phrases such as "experts agree," "numerous studies demonstrate," or "many critics believe" without identifiable sources.

12\. Do not exaggerate the amount of evidence. One or two publications do not justify claims such as "extensively documented" or "supported by numerous investigations."

13\. Do not attribute your own analysis to sources. Distinguish what a publication explicitly states from interpretations developed afterward.

14\. Do not invent implications. Chronological relationships do not automatically establish causation, influence, or intent.

15\. Avoid artificial sections about challenges and future prospects. Do not automatically add sections titled "Challenges," "Opportunities," "Future Outlook," or "Legacy."

16\. Do not introduce generic awards or recognition. Include only identifiable distinctions relevant to the subject.

17\. Avoid fabricated ecological connections. When discussing animals or plants, do not add generic statements about environmental balance, biodiversity, or conservation without specific evidence.

18\. Do not replace specific facts with vague praise. Preserve relevant names, dates, actions, quantities, and circumstances.

## 2. Language, Vocabulary, and Sentence Construction

19\. Avoid statistically repetitive AI vocabulary. The publication identifies the following English expressions as frequently overused:

`additionally` (especially opening a sentence), `align with`, `boasts` (meaning "has"), `bolstered`, `crucial`, `deep dive`, `delve`, `emphasizing`, `enduring`, `enhance`, `fostering`, `garner`, `highlight` (as a verb), `interplay`, `intricate`, `key` (as an adjective), `landscape` (as an abstract noun), `meticulous`, `pivotal`, `robust`, `showcase`, `tapestry` (as an abstract noun), `testament`, `underscore` (as a verb), `valuable`, `vibrant`.

20\. Track vocabulary by model generation. The publication separates two eras, and they should not be merged into one list.

- Mid-2025 to mid-2026 (GPT-5 era): `emphasizing`, `enhance`, `highlighting`, `showcasing`, plus the words tied to canned emphasis on notability, attribution, and media coverage.
- Mid-2026 onward (GPT-6 era): `challenge`, `clearer`, `dependable`, `echoed`, `foster`, `leverage`, `matters`, `multifaceted`, `practical`, `prioritize`, `quietly`, `steady`, `universally`. This era also shows heavier use of periods and commas and short sentences held to a strict 8 to 20 word band.

These words are not forbidden. Mechanical repetition and clustering are the problem. Marker-word lists age quickly, so rely on the structural rules more than on any list.

21\. Prefer direct verbs. Avoid constantly replacing "is," "has," "does," or "uses" with "represents," "constitutes," "offers," "functions as," or "positions itself as."

22\. Do not overcomplicate simple definitions. "It is an automation tool" is usually more natural than "It represents a technological solution designed to enhance operational processes."

23\. Avoid repetitive negative parallelism, particularly:

- "Not only X, but also Y."
- "It's not about X, it's about Y."
- "It's more than X; it's Y."
- "Not X. Not Y. Just Z."
- "Y rather than X," when the contrast is unnecessary.

24\. Do not turn every explanation into a correction of an imagined misconception. Do not assume the reader has misunderstood the subject.

25\. Avoid automatically applying the rule of three. Do not force expressions such as "efficient, robust, and scalable" or "analyze, optimize, and transform" when three elements are unnecessary.

26\. Avoid false ranges. Do not use "from X to Y" to suggest a spectrum that the text never establishes. "From intimate gatherings to global movements" implies breadth without demonstrating any. Use "from X to Y" only when X and Y are real endpoints of a measurable or ordered range, and name the items directly otherwise.

27\. Avoid attaching interpretive participial phrases to every sentence. Example: "The company opened another office, strengthening its position, reinforcing its presence, and demonstrating its commitment."

28\. Avoid mechanical transitions. Do not repeatedly begin paragraphs with "Additionally," "Furthermore," "Moreover," "On the other hand," "Consequently," or "It is worth noting."

29\. Do not replace simple words with unnecessarily sophisticated synonyms. Prefer "wrote," "used," "moved," or "tried" when these communicate the intended meaning better than elaborate alternatives.

30\. Do not change terminology solely to avoid repetition. Maintain consistent vocabulary, especially in technical explanations.

31\. Vary sentence length and structure naturally. Avoid producing sequences of sentences with nearly identical lengths, including runs of short sentences that all fall in the same narrow word band.

32\. Avoid excessively uniform punctuation. Do not construct every paragraph from short sentences separated by periods and commas in predictable patterns.

33\. Do not overuse em dashes (`—`). Use them when grammatically appropriate rather than as a constant stylistic decoration. A comma, colon, or period often works better.

34\. Do not artificially eliminate every em dash. Completely avoiding a legitimate punctuation mark creates another mechanical pattern. This rule and rule 33 are the single reference for em dash use.

35\. Use en dashes (`–`) for ranges of dates, numbers, pages, and scores (1990–2000, pp. 45–60, 3–2). Models often substitute a hyphen (`-`) where an en dash belongs. Keep hyphens for compound words and em dashes for breaks in a sentence. Follow the destination's convention when it requires plain hyphens.

36\. Avoid repetitive opening formulas. Do not systematically begin with phrases such as "In today's rapidly evolving world" or "In the current landscape."

37\. Preserve nuance without manufacturing ambiguity. Make direct statements when evidence supports them and introduce qualifications when uncertainty genuinely exists.

## 3. Formatting and Visual Structure

38\. Do not use bold formatting systematically. Reserve emphasis for situations where it genuinely improves readability.

39\. Avoid unnecessary lists with bold headings followed by colons. Repeated structures such as `- **Concept:** explanation` are among the patterns identified in the publication.

40\. Do not turn every explanation into a list. Use paragraphs when ideas have a natural narrative or argumentative relationship.

41\. Do not create unnecessary tables. Use tables only when they make comparisons or structured data easier to understand.

42\. Avoid excessive title capitalization. Prefer sentence case for headings unless the language, publication, or style guide requires title case.

43\. Do not add headings to short responses. A two-paragraph explanation generally does not require three separate sections.

44\. Do not repeat a document's title as the first heading when the destination already provides it.

45\. Maintain a consistent heading hierarchy. Do not skip heading levels or use top-level headings where subsections are appropriate.

46\. Avoid empty headings. Each section should contain meaningful information rather than only additional headings.

47\. Do not insert horizontal separators automatically. Avoid adding `---` between every section.

48\. Do not use emojis as structural decoration. Especially avoid them in headings, lists, professional documents, and encyclopedic writing.

49\. Use Markdown only when appropriate for the destination. Do not insert `##`, `**text**`, or fenced code blocks into platforms that require different formatting. This is currently one of the most common signs, so verify the destination before formatting.

50\. `[W]` Do not mix incompatible markup languages. For example, avoid combining Markdown with MediaWiki's wikitext.

51\. Maintain consistent typography. Avoid arbitrarily mixing straight and curly quotation marks. The publication identifies this behavior in some models, although it is not reliable evidence of AI authorship by itself.

## 4. Communication and Conversational Behavior

52\. Eliminate automatic introductions. Avoid "Of course!", "Certainly!", "Great question!", "Absolutely!", or "Here's a detailed breakdown" when they add no value.

53\. Do not automatically praise or validate the user. Avoid "You're absolutely right," "That's an excellent observation," or "That's a brilliant strategy" without genuine evaluation.

54\. Do not systematically end responses by offering more help. Avoid concluding every answer with "Let me know if you need anything else," "I hope this helps," or "Would you like me to turn this into a table?"

55\. Do not include generation-process commentary in final content. Articles, emails, and documents should not contain instructions or remarks intended for the person who requested them.

56\. Do not leave editing instructions or placeholders in finished content. Remove expressions such as "Insert here," "Add source," "Replace this name," or unresolved template fields. Handle missing information separately or use an explicitly agreed placeholder convention.

57\. Avoid automatic instructional disclaimers. Do not insert "It is important to note that" or "It should be remembered that" without a concrete informational reason.

58\. Do not use generic disclaimers about source availability. Avoid "Public information is limited" or "Details are not widely documented" unless you have established that these statements are accurate.

59\. Do not add disclaimers about how sources should be used or interpreted. As of mid-2026, chatbots frequently add notes on the reliability or proper use of a source, similar to the didactic disclaimers common in GPT-4 output. State what the source says and cite it.

60\. Do not invent epistemic reservations. Expressions such as "this alone does not establish" or "this should be interpreted as X rather than Y" should respond to genuine uncertainty.

61\. Do not introduce unsolicited corrective comparisons. Avoid "This should not be confused with" when no confusion has been raised and there is no reasonable risk of misunderstanding.

62\. Do not include model knowledge-cutoff disclaimers inside authored content. Such statements concern the tool, not the subject of the text.

63\. Avoid repetitive conclusions. Do not add final sections that merely rephrase information already presented.

64\. Do not insert canned refusals or procedural apologies into material intended for publication. Communicate necessary limitations separately without embedding conversational artifacts in the final content.

65\. Do not deliver truncated content or conversation fragments. Ensure the final output is complete and contains no remnants of previous messages or generation controls.

## 5. Sources, References, and Verification

66\. Never fabricate bibliographic references. Do not invent titles, authors, publishers, or journals to support information that cannot be verified.

67\. Verify that links exist and lead to the correct resources. A working URL does not necessarily support the associated claim.

68\. Do not fabricate DOIs, ISBNs, PMIDs, or other identifiers. Verify that each identifier corresponds to the exact publication being cited.

69\. Do not cite entire books when a specific page reference is required. Include the relevant location whenever available.

70\. Do not use general sources as substitutes for specific evidence. A thematically related publication may not substantiate a particular claim.

71\. Do not fabricate quotations or author interpretations. Distinguish source quotations from original paraphrasing.

72\. Do not add decorative references. Every citation should support an identifiable claim.

73\. Do not generate unused references or undefined named references. Validate that all references are correctly declared and associated.

74\. Do not automatically include AI-tool tracking parameters in URLs. The publication identifies `utm_source=chatgpt.com`, `utm_source=openai`, `utm_source=copilot.com`, and `referrer=grok.com` as potential origin traces. Preserve parameters that are functionally necessary.

75\. Do not leave internal citation markers or system metadata in exported content. Check for artifacts such as:

- ChatGPT: `contentReference`, `oaicite`, `turn0search0`, `attributableIndex`.
- Gemini: `[cite: 1]`, `start_span`, `end_span`.
- Grok: `grok_card`, `grok_render_citation_card_json`.
- DeepSeek: markers such as `【85†L261-269】`.
- Perplexity: `[attached_file:1]`, `[web:1]`, `ppl-ai-file-upload`.
- Writing blocks: `:::writing`.

76\. `[W]` Do not invent platform-specific categories, templates, or parameters. In MediaWiki, verify that infoboxes, categories, and templates actually exist before using them.

77\. Do not copy references using formatting incompatible with the destination. Validate links, footnotes, reused references, and markup syntax.

## 6. Comments, Publications, and Change Logs

These rules derive from Wikipedia-specific sections. Rules tagged `[C]` also apply to GitHub, technical documentation, and content management systems. Rules tagged `[W]` apply only on Wikipedia.

78\. `[C]` Do not write ordinary comments like customer-service letters. Avoid formulas such as "I understand your concerns," "I appreciate your consideration," or "I have carefully reviewed your request" when the context calls for a direct response.

79\. `[C]` Do not turn ordinary comments into lengthy documents with multiple sections. Match the structure to the actual discussion.

80\. `[C]` Do not cite nonexistent policies, standards, or identifiers. Verify that every policy reference points to a real, applicable rule. Do not add canned assurances of compliance with guidelines either.

81\. `[C]` Do not respond to criticism with generic defenses about AI use. Address specific issues with evidence and disclose AI assistance when required.

82\. `[C]` Do not write change logs or edit summaries as self-promotional reports. Avoid formulas such as "Significantly improved clarity, coherence, neutrality, and overall quality."

83\. `[C]` Describe what actually changed. A change log should identify the concrete functional or editorial modification and, when relevant, its purpose.

84\. `[C]` Do not add generic compliance guarantees. Avoid "Ensured compliance with best practices" or "Guaranteed adherence to all standards" without actual verification.

85\. `[C]` Do not systematically document what was left unchanged. Formulas such as "Improved X while preserving Y and avoiding changes to Z" should be reserved for situations where preservation is relevant.

86\. `[C]` Do not overload change summaries with irrelevant technical parameter names. Include identifiers when necessary to understand or locate a modification.

87\. `[C]` Do not include artificial statements addressed to reviewers. Avoid self-congratulatory notes about a document's quality, neutrality, or acceptability.

88\. `[W]` Do not add maintenance or status templates without justification. On Wikipedia, the publication particularly warns against inserting rejection or protection templates before they apply.

89\. `[W]` Do not generate personal pages using identical generic structures. Avoid empty promotional templates such as "About Me," "My Interests," "My Contributions," and "Let's Connect."

90\. Maintain stylistic continuity when editing existing content. Do not abruptly transform an author's voice, terminology, or degree of formality without an editorial reason. Avoid large-scale edits that add little value, and make sure each modification serves a concrete, verifiable purpose rather than merely replacing words.

## 7. Additional Rules Derived from Historical Indicators

The publication notes that these patterns are more characteristic of earlier model generations and are less useful as present-day indicators.

91\. Do not introduce knowledge-cutoff statements unless necessary for interpreting the response.

92\. Do not add an "In Conclusion" or "In Summary" section solely to follow a template.

93\. Do not pursue lexical diversity by constantly replacing the same term with different synonyms.

94\. Do not reuse outdated bibliographic access dates as if they represented recent verification.

95\. Do not leave fragments truncated by generation limits or copying operations.

## 8. Quality Rules That Must Not Be Confused with AI Indicators

These complementary rules follow from the publication's warnings and limitations.

96\. Do not deliberately introduce spelling or grammatical errors to imitate human writing.

97\. Do not sacrifice accuracy for informality. Technical writing can be formal without sounding artificial.

98\. Do not remove legitimate citations merely because a text appears heavily documented.

99\. Do not absolutely prohibit individual words. Evaluate frequency, context, and necessity. Detection patterns are primarily associated with combinations and repetition.

100\. Do not treat statistical indicators as proof of authorship. Perfect grammar, formal language, Markdown, or punctuation alone cannot establish that a text was generated by AI.

101\. Do not conceal substantive problems through cosmetic editing. Correct unsupported claims, fabricated references, inaccurate attribution, and superficial analysis first. Maintain transparency about AI assistance whenever the context or applicable rules require it.

## Finding Severity Classification

Classify each audit finding using one of four severity levels:

- P0 — Critical: Factual inaccuracies, fabricated references, misleading claims, or serious source-integrity problems.
- P1 — High: Significant structural problems, unsupported significance claims, vague associations, and applicable high-frequency indicators identified by Wikipedia.
- P2 — Medium: Formulaic writing patterns, repetitive constructions, unnecessary transitions, unnatural phrasing, and clarity issues.
- P3 — Low: Minor stylistic inconsistencies, historical AI-writing indicators, and optional cosmetic improvements.

Every audit finding must include its severity (`P0`–`P3`), applicable rule ID, exact source text, recommended replacement, and justification.

## Universal Operational Standard

Apply these rules as a provider-independent editorial specification, with the following priority order:

1. Factual accuracy and traceability: Correct information, verifiable references, and explicit relationships.
2. Communication precision: Concrete ideas, proportional explanations, and no unnecessary interpretive filler.
3. Natural editorial style: Appropriate vocabulary, varied sentence construction, and minimal formulaic repetition.
4. Destination-compatible formatting: No internal artifacts, incompatible markup, or unnecessary structures.

When auditing a text, start with the five current-priority signs listed at the top, then work through the sections in the order above. Vocabulary checks come last.

Fundamental distinction: Content accuracy and verifiability are more important than cosmetic AI-writing indicators. A text without recognizable AI phrases can still be inaccurate, superficial, or fabricated.

The objective is to produce specific, verifiable, coherent, and natural writing while preserving the author's intended voice, regardless of which language model generates or edits it.

## Source and Attribution

Adapted from Wikipedia contributors, [Wikipedia:Signs of AI writing (WP:AISIGNS)](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) ([revision history](https://en.wikipedia.org/w/index.php?title=Wikipedia:Signs_of_AI_writing&action=history)), maintained by [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup). Distributed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/). This adaptation paraphrases and reorganizes the original guide into 101 operational rules, scope tags, severity classifications, and execution instructions for AI agents.