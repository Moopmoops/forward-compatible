# Wikipedia "Forward Compatibility" — Proposed Improvements

## Status
Draft for review. All proposed changes are sourced to citable material. The goal is to improve the article's accuracy and depth without introducing original research.

---

## Strategy
- **Frame as strengthening**, not correcting — the article has good examples but thin conceptual foundation
- **Acknowledge existing Talk page discussions** that our additions address:
  - Daask (2018): suggested this article is a spinoff of "Future proofing" and needs better summary style → our definitional strengthening helps clarify this relationship
  - Recurring upward/forward/backward terminology confusion (multiple threads) → the W3C TAG material provides clearer, source-grounded terminology
  - KevinBTheobald (2020): made the point that forward compatibility doesn't require original designers to have anticipated future use → our material supports this nuance
- **Don't touch examples or NUC section** — add substance above them, avoid stepping on existing contributions
- **Start on Talk page**, wait for soft consensus, then edit in stages

---

## Talk page post (ready to paste)

### Subject line:
Proposed additions: W3C TAG definitions, design principles, Postel's Law connection

### Body:

This article has good examples but could use stronger conceptual grounding. I'd like to propose some additions drawing on published W3C and IETF material that the article currently doesn't reference. This would also help address a few threads that have come up on this Talk page over the years.

**What I'd like to add:**

1. **W3C TAG definition in the lead** — The W3C Technical Architecture Group's [Extending and Versioning Languages](https://www.w3.org/2001/tag/doc/versioning) series provides a more precise definition: "a change in the definition of a language is forward compatible if consumers of the original language can correctly process text written for the evolved version of the language." This helps ground the concept in published standards work and gives the lead more substance.

2. **Design principles section** — The W3C TAG documented specific strategies that enable forward compatibility: the "must ignore unknowns" rule, the "must accept and discard unknowns" rule, and the "must accept and preserve unknowns" rule ([source](https://www.w3.org/2001/tag/doc/versioning-compatibility-strategies)). These show *how* forward compatibility is achieved in practice, not just what it is. The existing HTML section could be strengthened with this context — HTML was forward-compatible because it was *designed* to accept unknown markup, which is what allowed tags like `<img>` to be added without breaking existing browsers.

3. **Connection to Postel's Law** — Forward-compatible design is closely related to the robustness principle from RFC 761 (1980): "be conservative in what you do, be liberal in what you accept from others." The "liberal in what you accept" half describes the core stance of forward-compatible systems. The article on the [Robustness principle](https://en.wikipedia.org/wiki/Robustness_principle) already exists but isn't linked from here.

4. **Definitional challenges note** — W3C TAG member Dan Connolly described formally defining forward compatibility as ["still an open research problem"](https://lists.w3.org/Archives/Public/www-tag/2007Aug/0069.html) in 2007. This is notable — the concept is widely used but has resisted clean formalization, in part because it describes a relationship to future versions that don't yet exist. I think the article is more honest and more interesting if it acknowledges this.

A few notes on how this connects to earlier discussions on this page:

- The recurring confusion about whether "upward" means "forward" or "backward" (discussed in several threads above) reflects the deeper definitional challenge that the W3C material addresses directly.
- @Daask's [2018 observation](https://en.wikipedia.org/wiki/Talk:Forward_compatibility#Future_proof_relationship) that this article could be better understood in relation to "Future proofing" is relevant — clearer definitions here would help distinguish the two concepts.
- @KevinBTheobald's [point](https://en.wikipedia.org/wiki/Talk:Forward_compatibility#Forward_compatibility_of_television_signals) that forward compatibility doesn't require the original designers to have anticipated future use is a nuance that the W3C material supports — forward compatibility is about how a system *handles* what it doesn't recognize, not whether the designers foresaw specific future changes.

All sources are published W3C specifications, RFCs, or archived W3C mailing lists. Happy to share draft wikitext. ~~~~

---

## Proposed article changes (for after Talk page consensus)

### 1. Strengthen the lead definition

**Current:**
> Forward compatibility or upward compatibility is a design characteristic that allows a system to accept input intended for a later version of itself.

**Proposed addition (after current lead paragraph):**
> The W3C Technical Architecture Group defines a forward-compatible change more precisely: "a change in the definition of a language is forward compatible if consumers of the original language can correctly process text written for the evolved version of the language."[1] Achieving forward compatibility typically requires that systems be designed to accept or gracefully handle input they do not recognize, rather than rejecting it.[2]

**Sources:**
- [1] W3C TAG, "Extending and Versioning Languages: Terminology" — https://www.w3.org/2001/tag/doc/versioning
- [2] W3C TAG, "Extending and Versioning Languages: Compatibility Strategies" — https://www.w3.org/2001/tag/doc/versioning-compatibility-strategies

---

### 2. New section: "Design principles" (before Examples)

**Proposed text:**

#### Must-ignore and must-accept rules

The W3C Technical Architecture Group identified several design strategies that enable forward compatibility in language and protocol design:[1]

- **Must Ignore Unknowns**: Consumers must ignore any portion of input they do not recognize. This allows new features to be added by producers without breaking existing consumers.
- **Must Accept and Discard Unknowns**: Consumers must accept input containing unrecognized portions and discard what they cannot process, continuing to process the remainder.
- **Must Accept and Preserve Unknowns**: Consumers should accept and preserve unrecognized portions of input, even if they cannot process them, allowing the information to be passed through to other systems that may understand it.

HTML has followed the must-accept approach since its earliest versions, specifying that unknown markup should be accepted rather than rejected.[2] This design decision enabled later additions — such as the `<img>` tag — to be deployed without breaking existing browsers.

#### Relationship to the robustness principle

Forward-compatible design is closely related to the robustness principle (Postel's Law), articulated by Jon Postel in RFC 761 (1980): "Be conservative in what you do, be liberal in what you accept from others."[3] The "liberal in what you accept" half of this principle describes the core stance of forward-compatible systems: accepting input that may not conform to the system's current expectations.

**Sources:**
- [1] W3C TAG, "Extending and Versioning Languages: Compatibility Strategies" — https://www.w3.org/2001/tag/doc/versioning-compatibility-strategies
- [2] W3C TAG, "Extending and Versioning Languages Part 1" — https://www.w3.org/2001/tag/doc/versioning.html
- [3] RFC 761, Transmission Control Protocol — https://www.rfc-editor.org/rfc/rfc761 (also documented in RFC 1122)

---

### 3. New section: "Definitional challenges" (after Design principles)

**Proposed text:**

Despite wide practical use, forward compatibility has proven difficult to define formally. In 2007, W3C Technical Architecture Group member Dan Connolly described the formal definition of forward and backward compatibility as "still an open research problem," noting that attempts to create rigorous formal mappings had not been completed.[1][2] The difficulty arises in part because forward compatibility describes a relationship between a current system and future versions that do not yet exist — making it inherently harder to specify than backward compatibility, which relates to known prior versions.

**Sources:**
- [1] Dan Connolly, "definition of forward compatible/backward compatible still an open problem," W3C TAG mailing list, 24 August 2007 — https://lists.w3.org/Archives/Public/www-tag/2007Aug/0069.html
- [2] W3C TAG ISSUE-41: "What are good practices for designing extensible languages and for handling versioning?" — https://www.w3.org/2001/tag/group/track/issues/41

---

### 4. Strengthen existing HTML example

The article already has an HTML section. Rather than adding a separate example, strengthen the existing one by connecting it to the design principles above — explain that HTML's forward compatibility stems from the specific design decision to accept unknown markup.

---

## Edit staging order
1. First edit: Add W3C TAG definition to lead (least controversial, adding sourced definition)
2. Second edit: Add Postel's Law connection + internal wikilink to Robustness principle
3. Third edit: Add "Design principles" section with must-ignore/must-accept rules
4. Fourth edit: Add "Definitional challenges" note
5. Fifth edit (optional): Strengthen existing HTML example with design-principle context

## Notes on Wikipedia editorial standards
- All proposed additions sourced to published, citable documents (W3C specifications, RFCs, archived mailing lists)
- No original research — connecting existing published material the article doesn't currently reference
- Tone is neutral and encyclopedic
- Acknowledges and builds on existing Talk page discussions rather than ignoring them
- Improves internal linking (Robustness principle article)
- The "definitional challenges" section embraces honest complexity rather than pretending the concept is settled
