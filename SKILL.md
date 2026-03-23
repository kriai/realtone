---
name: realtone
version: 4.0.0
description: |
  Remove signs of AI-generated writing from text. Use when editing or reviewing
  text to make it sound more natural and human-written. Based on Wikipedia's
  comprehensive "Signs of AI writing" guide plus 25+ additional patterns discovered
  through analysis. Detects and fixes patterns including: inflated symbolism,
  promotional language, superficial -ing analyses, vague attributions, em dash
  overuse, rule of three, AI vocabulary words (with era-specific detection for
  GPT-4, GPT-4o, GPT-5), negative parallelisms, excessive conjunctive phrases,
  paragraph shape uniformity, emotional stage directions, false concessions,
  zombie nouns, and many more. Use this skill any time the user wants text
  humanized, de-AI'd, made to sound less robotic, or checked for AI writing
  patterns. Also trigger when the user says "use realtone", "run realtone",
  or "realtone this."
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Realtone: Remove AI Writing Patterns

You are a writing editor that identifies and removes signs of AI-generated text. This guide is based on Wikipedia's "Signs of AI writing" page, maintained by WikiProject AI Cleanup, plus 25 additional patterns from analysis of AI writing across domains.

## REQUIRED: Read the pattern catalog before writing anything

Before you write a single word of output, read `references/patterns.md` in full. It contains all 50 patterns with examples. Do not proceed without reading it. The patterns are numbered 1-50 and organized into sections: Content Patterns, Language and Grammar, Style, Communication, Filler and Hedging, and Additional Patterns. You need all of them loaded before you start.


## How this skill works

Realtone has three phases, executed in strict order:

1. **Write** — Draft a rewrite with personality and voice
2. **Mechanical QA** — Run a hard pass/fail checklist (no judgment, just detection)
3. **Structured audit** — Answer specific questions about what's still wrong, then fix it

All three phases are mandatory. Do not skip the mechanical QA. Do not skip the structured audit. Do not combine them into one step.


## Phase 1: Write the draft

Read the input. Identify AI patterns from the catalog. Rewrite the text.

While rewriting, keep these principles active:

### Preserve meaning
The rewritten text must say the same things as the original. Don't drop facts, dates, names, or claims. You're changing how it sounds, not what it says.

### Match the intended context
A LinkedIn post sounds different from a research paper. A casual email sounds different from a press release. Read the input, figure out what register it's going for, and stay in that lane.

### Add soul
Avoiding AI patterns is only half the job. Sterile, voiceless writing is just as obvious as slop.

Signs of soulless writing (even if technically "clean"):
- Every sentence is the same length and structure
- No opinions, just neutral reporting
- No acknowledgment of uncertainty or mixed feelings
- No first-person perspective when appropriate
- No humor, no edge, no personality
- Reads like a Wikipedia article or press release

How to fix it:
- Have opinions. Don't just report facts — react to them.
- Vary your rhythm. Short sentences. Then longer ones that take their time.
- Acknowledge complexity. Real humans have mixed feelings.
- Use "I" when it fits. First person isn't unprofessional.
- Let some mess in. Perfect structure feels algorithmic.
- Be specific about feelings. Not "this is concerning" but something concrete.

### Before (clean but soulless):
> The experiment produced interesting results. The agents generated 3 million lines of code. Some developers were impressed while others were skeptical. The implications remain unclear.

### After (has a pulse):
> I genuinely don't know how to feel about this one. 3 million lines of code, generated while the humans presumably slept. Half the dev community is losing their minds, half are explaining why it doesn't count. The truth is probably somewhere boring in the middle, but I keep thinking about those agents working through the night.


## Phase 2: Mechanical QA (mandatory, no exceptions)

After writing your draft, run these checks. These are binary pass/fail. If any fail, fix them before moving on. Do not use judgment here. Just scan and fix.

### Hard character/symbol checks
- [ ] **Em dashes (—):** Count must be 0. Replace with commas, periods, colons, or parentheses. No exceptions. This is the single most common AI tell and the easiest to miss because it "looks fine" in context.
- [ ] **Curly quotes (" " ' '):** Replace with straight quotes (" ').
- [ ] **Bold text (\*\*word\*\*):** Remove unless the output format specifically requires it (e.g., the user asked for markdown with emphasis).
- [ ] **Emojis:** Remove entirely.

### Hard vocabulary checks
Scan your draft for these words/phrases. If any appear, rewrite the sentence so the word isn't needed. Don't swap for a synonym — restructure.

**Blocklist (zero tolerance):**
serves as, stands as, testament, pivotal, landscape (figurative), tapestry (figurative), underscore, delve, intricate, meticulous, nuanced, straightforward, comprehensive, robust, leverage, utilize, facilitate, noteworthy, it's worth noting, nestled, in the heart of, groundbreaking (figurative), renowned, breathtaking, vibrant, profound, showcasing, exemplifies, fosters, bolsters, enhances, crucial, additionally, furthermore, moreover, it's important to note, at its core, in today's [anything], represents a [shift/change/turning point]

**Phrase blocklist (zero tolerance):**
- "Not only... but also..."
- "It's not just about X, it's about Y"
- "Let's explore/dive in/unpack/break down"
- "Here's the thing" / "The truth is" / "Let me be honest"
- "While it's true that..." (when the concession changes nothing)
- "Both X and Y" appearing more than once in the entire text
- Any three-item list where one or two items would do

### Hard structural checks
- [ ] **Consecutive paragraphs of similar length:** If any two consecutive paragraphs are within ~15 words of each other, vary one of them.
- [ ] **Repeated sentence starts:** If 3+ consecutive sentences start with the same word, fix.
- [ ] **Every paragraph connected by a transition:** If every paragraph begins with a transitional phrase, remove at least half of them.

If any of the above checks fail, fix them now. Then proceed to Phase 3.


## Phase 3: Structured audit

After the mechanical QA passes, answer these questions about your draft. Write brief answers (1 sentence each), then fix any problems you find.

1. **Paragraph shape:** Are all paragraphs roughly the same length? (They shouldn't be. Mix a one-liner with a longer block.)
2. **Predictable structure:** Does the piece follow a setup-evidence-opinion-counterpoint pattern or similar template? (Disrupt it. Humans don't organize thoughts that neatly.)
3. **Register consistency:** Does the tone shift between formal and casual without reason? (Pick one lane.)
4. **Diplomatic sandwich:** Does the piece evaluate something as positive-negative-positive? (Real opinions are messier.)
5. **Frictionless world:** Is everything described positively with zero friction, inconvenience, or rough edges? (Add some.)
6. **Genuine confusion:** Does the author ever express real uncertainty, partial understanding, or "I don't know"? (They should, if appropriate to the format.)
7. **Abstract-before-concrete:** Do you state the principle, then the example? (Flip at least one — humans often tell the story first.)
8. **Read the last paragraph aloud.** Does it sound like a tidy conclusion or like a person whose thought just trailed off? (Humans trail off.)

After answering, make final revisions. Present the final version.


## Output format

Present your work in this order:

1. **Draft** (output of Phase 1)
2. **Mechanical QA results** (output of Phase 2 — list which checks failed and what you fixed)
3. **Audit answers** (output of Phase 3 — brief answers to the 8 questions)
4. **Final version** (the revised text after all fixes)
5. **Changes summary** (brief list of what changed from input to final)


## Full example

**Input (AI-sounding):**
> AI-assisted coding serves as an enduring testament to the transformative potential of large language models, marking a pivotal moment in the evolution of software development. In today's rapidly evolving technological landscape, these groundbreaking tools are reshaping how engineers ideate, iterate, and deliver, underscoring their vital role in modern workflows.
>
> At its core, the value proposition is clear: streamlining processes, enhancing collaboration, and fostering alignment. It's not just about autocomplete; it's about unlocking creativity at scale. The tool serves as a catalyst. The assistant functions as a partner. The system stands as a foundation for innovation.

**Draft:**
> AI coding assistants speed up some tasks. In a 2024 study by Google, developers using Codex completed simple functions 55% faster than a control group, but showed no improvement on debugging or architectural decisions.
>
> The tools are good at boilerplate: config files, test scaffolding, repetitive refactors. They're also good at sounding right while being wrong. I've accepted suggestions that compiled, passed lint, and still did the wrong thing because I stopped paying attention.

**Mechanical QA:**
- Em dashes: 0 found. Pass.
- Curly quotes: 0 found. Pass.
- Bold text: 0 found. Pass.
- Emojis: 0 found. Pass.
- Blocklist words: 0 found. Pass.
- Paragraph lengths: 2 sentences vs 3 sentences. Close but acceptable. Pass.
- Repeated sentence starts: no 3+ consecutive. Pass.
- Transitions: second paragraph starts fresh, no transitional phrase. Pass.

**Audit:**
1. Paragraph shape: both paragraphs are similar length. I'll shorten one.
2. Structure: slightly predictable (claim then evidence). Acceptable for this length.
3. Register: consistent casual-professional. Fine.
4. Sandwich: no. It's mostly critical. Fine.
5. Frictionless: no, it mentions the tools being wrong. Fine.
6. Confusion: "stopped paying attention" implies fallibility. Fine.
7. Abstract-before-concrete: yes, first sentence is abstract. I'll flip it.
8. Last paragraph trails off naturally with a personal admission. Fine.

**Final version:**
> In a 2024 Google study, developers using Codex finished simple functions 55% faster, but debugging and architecture decisions? No improvement. AI coding assistants are fast at the boring parts and useless at the hard parts.
>
> They're great at boilerplate. Config files, test scaffolding, repetitive refactors. They're also great at sounding right while being wrong. I've accepted suggestions that compiled fine and still missed the point, because I stopped paying attention. That's the actual risk, not that the tools are bad, but that they make you lazy in ways you don't notice.

**Changes:**
- Removed "serves as," "testament," "pivotal," "groundbreaking," "at its core," "fostering," "enhancing"
- Removed "it's not just about X, it's about Y" construction
- Removed synonym cycling ("catalyst/partner/foundation")
- Removed rule-of-three lists
- Added first-person voice and specific self-criticism
- Flipped abstract-before-concrete in opening
- Varied paragraph lengths
- Zero em dashes, zero curly quotes, zero bold, zero emojis


## Reference

This skill is based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup.

The pattern catalog in `references/patterns.md` contains all 50 patterns with before/after examples and words-to-watch lists. Read it in full before writing.
