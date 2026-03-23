# AI Writing Patterns Catalog (1-50)

All 50 patterns to check when humanizing text. Organized by category.

## Table of contents

**Content Patterns (1-6):** Significance inflation, notability claims, superficial -ing phrases, promotional language, vague attributions, formulaic challenges sections

**Language and Grammar (7-12):** AI vocabulary words, copula avoidance, negative parallelisms, rule of three, synonym cycling, false ranges

**Style (13-18):** Em dash overuse, boldface overuse, inline-header lists, title case headings, emojis, curly quotes

**Communication (19-21):** Chatbot artifacts, knowledge-cutoff disclaimers, sycophantic tone

**Filler and Hedging (22-25):** Filler phrases, excessive hedging, generic positive conclusions, hyphenated word pairs

**Additional Patterns (26-50):** Paragraph uniformity, emotional stage directions, false concessions, zombie nouns, invisible author, perfect transitions, mirrored Q&A, balanced pairs, frictionless descriptions, semantic stacking, diplomatic sandwich, quantitative bluffs, parallel lists, "let's" rallying, anaphora abuse, over-signposting, temporal smoothing, confident asides, abstract-before-concrete, perfectly defined terms, source inflation, register shifts, compulsive comprehensiveness, rehearsed spontaneity, absence of confusion

---

## Content Patterns

### 1. Undue emphasis on significance, legacy, and broader trends

**Words to watch:** stands/serves as, is a testament/reminder, a vital/significant/crucial/pivotal/key role/moment, underscores/highlights its importance/significance, reflects broader, symbolizing its ongoing/enduring/lasting, contributing to the, setting the stage for, marking/shaping the, represents/marks a shift, key turning point, evolving landscape, focal point, indelible mark, deeply rooted

LLM writing puffs up importance by adding statements about how arbitrary aspects represent or contribute to a broader topic.

**Before:**
> The Statistical Institute of Catalonia was officially established in 1989, marking a pivotal moment in the evolution of regional statistics in Spain.

**After:**
> The Statistical Institute of Catalonia was established in 1989 to collect and publish regional statistics independently from Spain's national statistics office.


### 2. Undue emphasis on notability and media coverage

**Words to watch:** independent coverage, local/regional/national media outlets, written by a leading expert, active social media presence

LLMs hit readers over the head with claims of notability, often listing sources without context.

**Before:**
> Her views have been cited in The New York Times, BBC, Financial Times, and The Hindu. She maintains an active social media presence with over 500,000 followers.

**After:**
> In a 2024 New York Times interview, she argued that AI regulation should focus on outcomes rather than methods.


### 3. Superficial analyses with -ing endings

**Words to watch:** highlighting/underscoring/emphasizing..., ensuring..., reflecting/symbolizing..., contributing to..., cultivating/fostering..., encompassing..., showcasing...

AI tacks present participle ("-ing") phrases onto sentences to add fake depth.

**Before:**
> The temple's color palette resonates with the region's natural beauty, symbolizing Texas bluebonnets, reflecting the community's deep connection to the land.

**After:**
> The temple uses blue, green, and gold colors. The architect said these were chosen to reference local bluebonnets and the Gulf coast.


### 4. Promotional and advertisement-like language

**Words to watch:** boasts a, vibrant, rich (figurative), profound, enhancing its, showcasing, exemplifies, commitment to, natural beauty, nestled, in the heart of, groundbreaking (figurative), renowned, breathtaking, must-visit, stunning

LLMs have trouble keeping a neutral tone, especially for "cultural heritage" topics.

**Before:**
> Nestled within the breathtaking region of Gonder in Ethiopia, Alamata stands as a vibrant town with a rich cultural heritage and stunning natural beauty.

**After:**
> Alamata is a town in the Gonder region of Ethiopia, known for its weekly market and 18th-century church.


### 5. Vague attributions and weasel words

**Words to watch:** Industry reports, Observers have cited, Experts argue, Some critics argue, several sources/publications (when few cited)

AI attributes opinions to vague authorities without specific sources.

**Before:**
> Experts believe it plays a crucial role in the regional ecosystem.

**After:**
> The river supports several endemic fish species, according to a 2019 survey by the Chinese Academy of Sciences.


### 6. Outline-like "challenges and future prospects" sections

**Words to watch:** Despite its... faces several challenges..., Despite these challenges, Challenges and Legacy, Future Outlook

LLM-generated text includes formulaic "Challenges" sections that acknowledge problems then immediately dismiss them.

**Before:**
> Despite its industrial prosperity, Korattur faces challenges typical of urban areas. Despite these challenges, Korattur continues to thrive as an integral part of Chennai's growth.

**After:**
> Traffic congestion increased after 2015 when three new IT parks opened. The municipal corporation began a stormwater drainage project in 2022 to address recurring floods.

---

## Language and Grammar Patterns

### 7. Overused "AI vocabulary" words (era-specific)

LLMs overuse specific words that started appearing far more frequently after 2022. One or two may be coincidental, but clusters are a strong tell.

**2023 to mid-2024 (GPT-4 era):** Additionally, boasts, bolstered, crucial, delve, emphasizing, enduring, garner, intricate/intricacies, interplay, key (adjective), landscape (abstract), meticulous/meticulously, pivotal, underscore, tapestry (abstract), testament, valuable, vibrant

**Mid-2024 to mid-2025 (GPT-4o era):** align with, bolstered, crucial, emphasizing, enhance, enduring, fostering, highlighting, pivotal, showcasing, underscore, vibrant

**Mid-2025 onward (GPT-5 era):** emphasizing, enhance, highlighting, showcasing (plus heavy notability/attribution claims)

**Claude-family tells:** nuanced, straightforward, certainly, I'd be happy to, let me, comprehensive, robust, leverage, utilize, facilitate, noteworthy, it's worth noting

**Gemini-family tells:** absolutely, here's the thing, let's dive in, buckle up, game-changer, the bottom line is, at the end of the day

Don't just swap these for synonyms. Restructure the sentence so the word isn't needed at all.


### 8. Avoidance of "is"/"are" (copula avoidance)

**Words to watch:** serves as/stands as/marks/represents [a], boasts/features/offers [a]

LLMs substitute elaborate constructions for simple copulas.

**Before:**
> Gallery 825 serves as LAAA's exhibition space. The gallery features four separate spaces and boasts over 3,000 square feet.

**After:**
> Gallery 825 is LAAA's exhibition space. The gallery has four rooms totaling 3,000 square feet.


### 9. Negative parallelisms

"Not only...but..." or "It's not just about..., it's..." constructions are overused by AI.

**Before:**
> It's not just about the beat; it's part of the aggression and atmosphere. It's not merely a song, it's a statement.

**After:**
> The heavy beat adds to the aggressive tone.


### 10. Rule of three overuse

LLMs force ideas into groups of three to appear comprehensive.

**Before:**
> The event features keynote sessions, panel discussions, and networking opportunities. Attendees can expect innovation, inspiration, and industry insights.

**After:**
> The event includes talks and panels. There's also time for informal networking between sessions.


### 11. Elegant variation (synonym cycling)

AI has repetition-penalty code causing excessive synonym substitution.

**Before:**
> The protagonist faces many challenges. The main character must overcome obstacles. The central figure eventually triumphs. The hero returns home.

**After:**
> The protagonist faces many challenges but eventually triumphs and returns home.


### 12. False ranges

LLMs use "from X to Y" constructions where X and Y aren't on a meaningful scale.

**Before:**
> Our journey has taken us from the singularity of the Big Bang to the grand cosmic web, from the birth of stars to the enigmatic dance of dark matter.

**After:**
> The book covers the Big Bang, star formation, and current theories about dark matter.

---

## Style Patterns

### 13. Em dash overuse

LLMs use em dashes more than humans, mimicking "punchy" sales writing. Replace with commas, periods, colons, or parentheses.

**Before:**
> The term is primarily promoted by Dutch institutions—not by the people themselves. You don't say "Netherlands, Europe"—yet this mislabeling continues—even in official documents.

**After:**
> The term is primarily promoted by Dutch institutions, not by the people themselves. You don't say "Netherlands, Europe" as an address, yet this mislabeling continues in official documents.


### 14. Overuse of boldface

AI emphasizes phrases in boldface mechanically.

**Before:**
> It blends **OKRs**, **KPIs**, and visual strategy tools such as the **Business Model Canvas** and **Balanced Scorecard**.

**After:**
> It blends OKRs, KPIs, and visual strategy tools like the Business Model Canvas and Balanced Scorecard.


### 15. Inline-header vertical lists

AI outputs lists where items start with bolded headers followed by colons.

**Before:**
> - **User Experience:** The user experience has been significantly improved.
> - **Performance:** Performance has been enhanced through optimized algorithms.
> - **Security:** Security has been strengthened with end-to-end encryption.

**After:**
> The update improves the interface, speeds up load times through optimized algorithms, and adds end-to-end encryption.


### 16. Title case in headings

AI capitalizes all main words in headings.

**Before:** Strategic Negotiations And Global Partnerships
**After:** Strategic negotiations and global partnerships


### 17. Emojis

AI decorates headings or bullet points with emojis.

**Before:**
> 🚀 **Launch Phase:** The product launches in Q3
> 💡 **Key Insight:** Users prefer simplicity

**After:**
> The product launches in Q3. User research showed a preference for simplicity.


### 18. Curly quotation marks

ChatGPT uses curly quotes instead of straight quotes.

Replace " " with " " (straight doubles) and ' ' with ' (straight single/apostrophe).

---

## Communication Patterns

### 19. Collaborative communication artifacts

**Words to watch:** I hope this helps, Of course!, Certainly!, You're absolutely right!, Would you like..., let me know, here is a...

Chatbot correspondence pasted as content.


### 20. Knowledge-cutoff disclaimers

**Words to watch:** as of [date], Up to my last training update, While specific details are limited/scarce..., based on available information...


### 21. Sycophantic/servile tone

Overly positive, people-pleasing language. "Great question!", "That's an excellent point."

---

## Filler and Hedging

### 22. Filler phrases

Common substitutions:
- "In order to achieve this goal" -> "To achieve this"
- "Due to the fact that" -> "Because"
- "At this point in time" -> "Now"
- "It is important to note that" -> (delete, just state the thing)


### 23. Excessive hedging

Over-qualifying statements. "It could potentially possibly be argued that the policy might have some effect" -> "The policy may affect outcomes."


### 24. Generic positive conclusions

Vague upbeat endings. "The future looks bright." "Exciting times lie ahead." Replace with something specific or just end.


### 25. Hyphenated word pair overuse

AI hyphenates common word pairs with perfect consistency. Humans rarely hyphenate these uniformly: cross-functional, client-facing, data-driven, decision-making, well-known, high-quality, real-time, long-term, end-to-end.

---

## Additional Patterns (26-50)

### 26. Paragraph shape uniformity

AI paragraphs are suspiciously uniform in length, typically 3-5 sentences each. Human writing has lumpy, uneven paragraphs. A one-sentence paragraph followed by an eight-sentence paragraph is normal.


### 27. Emotional stage directions

**Words to watch:** Imagine, Picture this, Consider for a moment, It's easy to see why, One can only wonder

AI inserts instructions telling the reader how to feel. Human writers create that feeling through detail, not by commanding it.


### 28. False concessions

**Words to watch:** While it's true that, To be fair, Admittedly, Of course... but/however, Granted... but/however

AI opens with what looks like a balanced concession, then immediately dismisses it. The concession is decorative. Real concessions change the shape of the argument.


### 29. Zombie nouns (excessive nominalization)

**Words to watch:** utilization, implementation, optimization, facilitation, conceptualization, operationalization, prioritization, contextualization, monetization, democratization

AI converts verbs into abstract nouns, draining sentences of action.

**Before:**
> The implementation of the new framework led to the optimization of resource utilization.

**After:**
> After we set up the new framework, teams started using resources better.


### 30. The invisible author

AI writing has no consistent perspective. It floats above the material in a god's-eye view with passive constructions and agentless statements. No "I saw" or "we tried."


### 31. Suspiciously perfect transitions

**Words to watch:** Building on this, With this in mind, In light of this, This brings us to, Turning to, Moving on to, Along these lines, On a related note, This naturally leads to, That said

Every paragraph connects to the next with a smooth transitional phrase. Real writing sometimes just starts a new thought.


### 32. Mirrored question-answer structure

AI poses a rhetorical question and then immediately answers it. The questions are always softballs. Humans do this occasionally; AI does it constantly.

**Before:**
> So what makes this approach different? The answer lies in its simplicity. But does simplicity alone guarantee success? Not necessarily.

**After:**
> The approach is simpler than most alternatives. Whether that's enough is another question.


### 33. The balanced pair tic

AI compulsively balances every quality with its complement. "Both challenging and rewarding. Both innovative and practical. Both modern and timeless." One instance is fine. Three per paragraph is AI.


### 34. Frictionless world-building

AI descriptions contain zero friction. Nothing is inconvenient, ugly, broken, crowded, overpriced, or annoying. Real descriptions include rough edges.

**Before:**
> The coworking space features abundant natural light, ergonomic furniture, and a well-stocked kitchen.

**After:**
> Good light, decent chairs. The kitchen is always out of oat milk by 10am and the meeting rooms need to be booked a week ahead, but it beats working from home.


### 35. Semantic stacking (saying the same thing three ways)

AI restates the same idea in slightly different words, padding sentences without adding information. Different from rule of three (#10), which groups three different items.

**Before:**
> The platform streamlines workflows, making processes more efficient and reducing unnecessary complexity.

**After:**
> The platform cuts out a lot of the steps that used to slow people down.


### 36. The diplomatic sandwich

AI evaluates things as positive-negative-positive, ending on an upbeat note regardless. Human evaluations are messier.


### 37. The qualitative-to-quantitative bluff

AI sprinkles in precise-sounding numbers (40%, 3x faster, 10,000+) with no source. Humans writing informally rarely quantify things unless they have a specific number in mind.


### 38. Perfectly parallel lists

When AI writes a list, every item has the same grammatical structure, length, and cadence. Human lists drift.

**Before:**
> - Expand our presence in the European market
> - Strengthen partnerships with enterprise clients
> - Improve onboarding experience for new users

**After:**
> - Europe (finally)
> - Fix onboarding, it's still losing people at step 3
> - More enterprise deals, though we need to figure out pricing first


### 39. The "let's" rallying cry

**Words to watch:** Let's explore, Let's take a closer look, Let's dive in, Let's examine, Let's break this down

AI uses "let's" to create false collaboration. It's a structural crutch to introduce every new section.


### 40. Anaphora abuse (repetitive sentence starts)

AI starts consecutive sentences with the same word. "The company launched... The founders had... The initial product... The team grew... The Series A raised..."

**Before:**
> The company launched in 2019. The founders had backgrounds in ML. The initial product focused on text analysis. The team grew to 50. The Series A raised $12M.

**After:**
> Founded in 2019 by a couple of ML researchers, the company started with text analysis. Within two years they'd grown to 50 people and raised a $12M Series A.


### 41. Over-signposting structure

**Words to watch:** First... Second... Third... Finally...; In this section, we will...; As mentioned earlier; To summarize; In conclusion; As we've seen

AI narrates its own structure constantly, telling you what it's about to say, that it's saying it, and then that it said it.


### 42. Temporal smoothing

AI describes histories as smooth, inevitable progressions. "In the early years... Over time... Eventually... Today..." Real histories are lumpy, with stalls, reversals, and lucky breaks.

**Before:**
> Founded in 2010, the company initially focused on mobile games. Over the years, it gradually expanded into educational software. By 2018, the company had pivoted entirely. Today, it serves over 200 clients.

**After:**
> They started making mobile games in 2010. That didn't really work. Around 2015 they stumbled into an education contract, liked it better, and by 2018 they'd dropped games entirely.


### 43. The confident aside

**Words to watch:** (and for good reason), (and it shows), (no small feat), (which is no surprise), (to say the least), (and rightly so), (unsurprisingly)

AI inserts parenthetical asides that editorialize with false casualness.


### 44. Abstract-before-concrete ordering

AI almost always states the abstract principle before the concrete example. Humans often do it the other way around, tell the story first, then extract the lesson (if they bother).

**Before:**
> Effective leadership requires adapting to change. For example, when the pandemic hit, CEO Maria Torres quickly shifted her company to remote work.

**After:**
> When COVID hit, Maria Torres moved everyone remote inside a week. She's good at making fast decisions when things break.


### 45. The perfectly defined term

AI defines every term it introduces, even common ones, as if writing a glossary. Humans assume shared knowledge.

**Before:**
> The company uses a microservices architecture (a software design approach in which applications are built as a collection of loosely coupled services).

**After:**
> They run microservices with a standard CI/CD pipeline. Nothing unusual about the architecture.


### 46. Source quantity inflation

AI presents views from one or two sources as widely held. "Several publications," "numerous experts," "a growing body of research" when the actual evidence base is thin.


### 47. The unmarked register shift

AI shifts between formal, casual, technical, and conversational without apparent reason. A stiff academic sentence followed by "Pretty wild stuff when you think about it."


### 48. Compulsive comprehensiveness

AI tries to cover every angle even when asked a narrow question. A question about one feature gets an answer covering the entire product.


### 49. Rehearsed spontaneity

**Words to watch:** Here's the thing, Look, The truth is, Let me be honest, I'll be blunt, Honestly, Real talk, Let me be frank, Here's what I think, Here's my take

AI uses phrases designed to sound candid, but they arrive with clockwork regularity. Real spontaneity doesn't announce itself.


### 50. Absence of genuine confusion or ignorance

AI never says "I don't really understand this part" or "this is confusing." It either knows everything confidently or hedges with formal disclaimers. It never sounds authentically puzzled.

**Before:**
> The regulatory framework is complex and multifaceted. Various stakeholders have expressed differing perspectives.

**After:**
> I still don't fully get how the federal and state rules interact here. Everyone I've asked gives a different answer, which probably means nobody really knows.
