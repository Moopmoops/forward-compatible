# Site Copy Review — Line-by-Line Proposals

Each entry identifies the current text, the problem, and a proposed alternative. Benjamin to approve, reject, or revise.

---

## Hero Section

### Subtitle
**Current:** "A framework for understanding how systems — biological, cultural, technological, institutional — meet futures they weren't built for."

**Problem:** "Weren't built for" implies the builders failed or were negligent. We discussed "weren't built specifically for" (awkward) and "couldn't have been built for" (absolute). The real point is that no system can anticipate everything — not a failing, just a condition.

**Proposal:** "A framework for understanding how systems — biological, cultural, technological, institutional — meet futures beyond what they were designed for."

"Beyond" frames it as a natural boundary rather than a deficiency. Open to other options.

### Meta-pattern
**Current:** "Someone included what the system was designed to exclude, and the system got better for everyone."

**Proposal:** "Someone included what the system was *previously* designed to exclude, and the system got better for everyone."

Already discussed and agreed — "previously" acknowledges the exclusion was a design boundary that made sense at the time.

---

## "Why This Matters" Section

### Opening paragraph
**Current:** "No individual can hold all the context needed for complex decisions. The future always contains information we don't have yet. Forward-compatible systems aren't just nice to have — they're necessary because closure is always premature given what we can't yet see."

**Problems (three, all discussed):**
1. "Nice to have" is unearned — nobody has argued FC is merely nice to have, so dismissing that position is a straw man
2. "Always" is an absolute
3. "Closure is always premature" is abstract — most readers won't immediately feel what "closure" means here

The first two sentences are good but serve distinct purposes (as Benjamin clarified: one is about human cognitive limits, the other about future unknowability). They should both stay but the third sentence needs rework.

**Proposal:** "No individual can hold all the context needed for complex decisions. The future always contains information we don't have yet. Every system eventually encounters something it wasn't designed for. The question is whether it breaks or adapts."

This grounds the abstract claim in something tangible — people can picture a system breaking.

### Callout box
**Current:** "FC isn't an alternative to your existing worldview. It's a lens for understanding what makes worldviews work — and how they can work for more people. Every worldview that ever worked got something right. Forward compatibility doesn't ask you to discard what works — it asks what else might be true alongside it."

**Problem:** This is mostly strong. But "FC isn't an alternative to your existing worldview" is slightly defensive — it anticipates an objection the reader may not be having yet. Starting with what FC *is* rather than what it *isn't* would be more affirming.

**Proposal:** "FC is a tool for understanding what makes worldviews work — and how they can work for more people. Forward compatibility asks what else might be true."

Dropping the negation and leading with the positive. Simpler, more confident.

### Paragraph after callout
**Current:** "When communities share frameworks for integrating perspectives, they collectively see more than any member can alone. FC's core pattern — include what's been excluded — is the mechanism that keeps this from collapsing into groupthink. The aspiration toward shared understanding is the method."

**Problem:** "The aspiration toward shared understanding *is* the method" is a strong line but it arrives without enough setup. The reader hasn't been told what the aspiration is or why it would be a method. Also "collapsing into groupthink" introduces a concern (groupthink) that the reader may not have been thinking about — it's defensive again.

**Proposal:** "When communities share frameworks for integrating perspectives, they collectively hold more context than any member can alone. Frameworks can  include new perspectives rather than enforcing existing ones. 

This grounds the claim (collective context > individual context).

---

## Principles Section

### Section intro
**Current:** "Forward compatibility is a fifty-year-old engineering concept that describes something deeper than engineering: the structural property that lets a system handle input that doesn't exist yet. It appears across biology, language, institutions, and culture — anywhere something lasts."

**Problem:** "Something deeper than engineering" is vague — deeper how? It risks sounding like the text is mystifying an engineering concept rather than extending it. Also "anywhere something lasts" is an unearned absolute — does FC really appear everywhere something lasts?

**Proposal:** "Forward compatibility started as an engineering concept — the structural property that lets a system handle input that doesn't exist yet. But the same pattern appears across biology, language, institutions, and culture. Wherever systems persist across time, the ones that can integrate what they weren't originally designed for tend to outlast the ones that can't."

More specific, grounded, and the "tend to" avoids the absolute.

### Principle 1: "Ignore what you don't understand"
**Current title:** "Ignore what you don't understand"

**Problem:** We discussed this extensively. "Ignore" sounds like "discard, it doesn't matter." The W3C's own progression shows the deeper design: ignore → accept and discard → accept and preserve. The most forward-compatible version holds what it doesn't understand rather than discarding it.

**Proposal for title:** "Prepare for what you don't yet understand"

**Current examples:** "Accept unknown input without breaking. HTML skipping unrecognized tags. A person hearing a new word and continuing the sentence."

**Proposal for examples:** "Don't break when you encounter something unfamiliar. HTML renders what it can and skips unrecognized tags — it doesn't reject the whole page. A person hearing a new word continues the conversation rather than stopping it."

More active, more vivid.  <Maybe we should swap #3 and #4 so it makes more sense. 

### Principle 4: "Leave room for what doesn't exist yet"
**Current examples:** "Build extensibility into the design. TCP's options field. Grammar broad enough to accept vocabulary that hasn't been coined. Protocol Buffers' field numbering that reserves space for future fields."

**Problem:** "Build extensibility into the design" is a command that restates the title — it doesn't add information. Protocol Buffers is a niche example most readers won't know.

**Proposal for examples:** "Design for inputs you can't predict. TCP's options field. Grammar broad enough to accept vocabulary that hasn't been coined. JSON's open key-value structure — any field can appear without breaking the format."

JSON is more widely understood and illustrates the same principle. <explain what this JSON example is to non-technical people>

### Principle 5: "Integrate the unknown"
**Current examples:** "Don't just skip or preserve unfamiliar input — learn from it. The immune system's memory cells. A person who encounters a new word eight times and becomes a different processor."

**Problem:** "Becomes a different processor" is clever but mechanical — it uses machine language for a human experience. It also understates what happens. When you learn a word, you don't just process differently — you understand more.

**Proposal for examples:** "Don't just skip or preserve unfamiliar input — learn from it. The immune system's memory cells remember every pathogen they've encountered and respond faster the next time. A person who encounters a new word enough times doesn't just know a new word — they can think thoughts they couldn't think before."

### Principle 8: "Ship stewardship alongside the system"
**Current examples:** "A technology isn't finished when it works. It's finished when you can describe the living system it enters — and how to tend that system's health while using it. Antibiotics without microbiome guidance. Social platforms without attention ecology guidance. The mechanical vocabulary had no conceptual slot for this — 'build, deploy, optimize' doesn't include 'tend.'"

**Problem:** The vocabulary argument at the end is making a point that belongs in the Vocabulary section, not here. It dilutes the principle. Also "attention ecology" may not land with most readers.

**Proposal for examples:** "A technology isn't finished when it works. It's finished when you can describe the living system it enters — and how to tend that system's health while using it. Antibiotics shipped without microbiome guidance. Social platforms launched without guidance on what they do to attention, trust, and community. The technology 'worked'; the ecology it entered was left untended."

Cleaner ending. Concrete instead of jargon.

---

## "What FC Does" Section

### Section intro
**Current:** "FC isn't just descriptive. It's a working tool."

**Problem:** "Isn't just descriptive" is another negation-first framing. And "working tool" is vague.

**Proposal:** "FC is a working tool — not just a way to describe systems, but a way to evaluate, compare, and design them."

### "Premium connector" role
**Current:** "Makes unrelated things legible as the same phenomenon. The immune system and HTML parsing are doing the same thing in different substrates. Knowledge transfers across domains."

**Problem:** "Premium connector" is an unusual phrase that doesn't immediately communicate what it means. "Knowledge transfers across domains" is passive and abstract.

**Proposal for title:** "Connector across domains"

**Proposal for description:** "Makes unrelated things visible as the same phenomenon. The immune system and HTML parsing are doing similar structural work in different substrates. Insights from one field become actionable in another."

### "Refiner of good and better"
**Current:** "Gives you answerable criteria. Does this system handle what it doesn't yet understand? Does it have room for what doesn't exist yet?"

**Problem:** "Refiner of good and better" is unclear as a title — refiner of what? The description is good but the title doesn't set it up.

**Proposal for title:** "Evaluative criteria"

**Proposal for description:** "Gives you specific, answerable questions to ask of any system. Does it handle what it doesn't yet understand? Does it have room for what doesn't exist yet? Does it protect the relationships that make it work?"

### "Empirical grounds for optimism"
**Current:** "Accumulated evidence that openness works — that systems which build room for the unknown outlast and outperform systems that close down. Not naive optimism. Architectural."

**Problem:** "Accumulated evidence that openness works" is an unsupported claim — the site hasn't presented this evidence yet. "Not naive optimism. Architectural." is a good line but it's doing defensive work ("not naive") before the positive claim has been earned.

**Proposal:** "The examples in this framework aren't cherry-picked success stories — they're a pattern that appears independently across biology, engineering, culture, and institutions. Systems that build room for the unknown tend to outlast systems that close down. That's not a wish. It's a structural observation."

---

## Vocabulary Section

### Opening paragraph
**Current:** "Twenty-first century technologies work with living systems — gene editing, microbiome cultivation, mRNA platforms, ecosystem management. You can't 'deploy' a microbiome. You cultivate it. The mechanical vocabulary ('build, deploy, optimize') didn't just lack precision — it closed off entire categories of responsibility. There was no conceptual slot for 'tend the living system this technology enters.'"

**Problem:** This implies the mechanical vocabulary is purely a thing of the past, and that 21st-century technologies are the reason we need ecological language. But as we discussed, ecological knowledge and vocabulary were always present — in farming, fermentation, medicine, midwifery. The shift isn't that technology changed; it's that ecological work is finally getting institutional recognition.

Also "There was no conceptual slot" is an absolute claim about the past. There *were* conceptual slots — in the traditions that used ecological vocabulary all along.

**Proposal:** "Technologies increasingly work with living systems — editing genomes, cultivating microbiomes, managing ecosystems. You can't 'deploy' a microbiome. You cultivate it. The mechanical vocabulary ('build, deploy, optimize') was precise for machines, but it closed off categories of responsibility that ecological work has always required. 'Tend the living system this enters' was always part of farming, fermentation, and medicine — it just wasn't part of the prestige vocabulary."

### Second paragraph
**Current:** "Ecological knowledge was always present alongside mechanical engineering — in farms, fermentation, medicine, soil. What changed isn't that we started doing ecological work. It's that we're finally giving it the vocabulary it deserves."

**Problem:** "The vocabulary it deserves" implies ecological work didn't have vocabulary — it did, abundantly. What it lacked was institutional recognition and prestige. Also this paragraph partially corrects the paragraph above it, which is awkward — the first paragraph should be right the first time.

**Proposal:** "Ecological knowledge was always present alongside mechanical engineering — in farms, fermentation, medicine, soil. What changed isn't that we started doing ecological work. It's that the work is finally gaining the recognition it has long warranted."

If the first paragraph is fixed as proposed above, this second paragraph can be shorter or folded in.

---

## Tradeoffs Section

### Section intro
**Current:** "Forward compatibility is not free. The costs are real and worth naming."

**Assessment:** This is good. Direct, honest, no wasted words. No change needed.

### Postel's Law paragraph
**Current:** "Postel's Law ('be liberal in what you accept') has a real critique: systems that are too tolerant can entrench flaws that become impossible to fix. TLS downgrade attacks exploit graceful degradation. FC takes the tradeoffs seriously — compatibility has costs, and naming them honestly is part of the work."

**Problem:** "FC takes the tradeoffs seriously" is the site speaking about itself in the third person, which sounds promotional. The rest is good.

**Proposal:** "Postel's Law ('be liberal in what you accept') has a real critique: systems that are too tolerant can entrench flaws that become impossible to fix. TLS downgrade attacks exploit graceful degradation. Compatibility has costs, and naming them honestly is part of the work."

Just drop the self-referential sentence.

---

## Examples Section

### Section intro
**Current:** "FC appears wherever systems persist across time. These aren't analogies — they're the same structural pattern in different substrates."

**Problem:** "These aren't analogies" is defensive — it preempts an objection. And "the same structural pattern in different substrates" is a strong claim that would need more argument to support. Are the immune system and HTML *really* doing the same thing, or are they doing structurally similar things?

**Proposal:** "FC appears wherever systems persist across time. These examples span biology, engineering, culture, and institutions — different domains, but a recognizable pattern across all of them."

More measured, still confident.

### Polyculture example
**Current:** "...in ways that looked like 'wilderness' to colonizers who only recognized monoculture rows as agriculture."

**Problem:** "Who only recognized monoculture rows as agriculture" is an oversimplification of colonial perception. Some colonizers did recognize Indigenous agriculture but chose to disregard it for political/economic reasons. The framing reduces complex colonial dynamics to a perceptual failure.

**Proposal:** "...in ways that were often not recognized as agriculture by colonizers whose frameworks defined farming as monoculture rows."

This locates the problem in the framework rather than claiming universal perceptual blindness.

---

## Items assessed as strong — no changes recommended

- Principle 2: "Negotiate to common ground" — clear, well-exampled
- Principle 3: "Degrade in layers rather than fail as a unit" — precise, good examples
- Principle 6: "Protect co-evolved relationships" — vivid, the Three Sisters example is strong
- Principle 7: "Maintain renewal mechanisms" — Ise Shrine example carries it
- Tradeoffs section intro: "Forward compatibility is not free. The costs are real and worth naming." — perfect
- Tradeoff tags: All clear and honest
- Most examples: NTSC, Ise Shrine, Curb Cut Effect, CRM are all strong
