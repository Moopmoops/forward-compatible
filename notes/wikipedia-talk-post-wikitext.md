# Wikipedia Talk Page Post — Ready to Paste as Wikitext

## Instructions
1. Go to Talk:Forward compatibility
2. Click "Add topic" (or "New section")
3. In the Subject/Headline field, paste the subject line below
4. In the body field, paste the body wikitext below
5. Click "Publish" — Wikipedia will auto-add your signature and timestamp

---

## Subject line:

Proposed additions: W3C TAG definitions, design principles, Postel's Law connection

## Body (paste this exactly):

This article has good examples but could use stronger conceptual grounding. I'd like to propose some additions drawing on published W3C and IETF material that the article currently doesn't reference. This would also help address a few threads that have come up on this Talk page over the years.

'''What I'd like to add:'''

'''1. W3C TAG definition in the lead''' — The W3C Technical Architecture Group's [https://www.w3.org/2001/tag/doc/versioning Extending and Versioning Languages] series provides a more precise definition: ''"a change in the definition of a language is forward compatible if consumers of the original language can correctly process text written for the evolved version of the language."'' This helps ground the concept in published standards work and gives the lead more substance.

'''2. Design principles section''' — The W3C TAG documented specific strategies that enable forward compatibility: the "must ignore unknowns" rule, the "must accept and discard unknowns" rule, and the "must accept and preserve unknowns" rule ([https://www.w3.org/2001/tag/doc/versioning-compatibility-strategies source]). These show ''how'' forward compatibility is achieved in practice, not just what it is. The existing HTML section could be strengthened with this context — HTML was forward-compatible because it was ''designed'' to accept unknown markup, which is what allowed tags like <code><img></code> to be added without breaking existing browsers.

'''3. Connection to Postel's Law''' — Forward-compatible design is closely related to the robustness principle from RFC 761 (1980): "be conservative in what you do, be liberal in what you accept from others." The "liberal in what you accept" half describes the core stance of forward-compatible systems. The article on the [[Robustness principle]] already exists but isn't linked from here.

'''4. Definitional challenges note''' — W3C TAG member Dan Connolly described formally defining forward compatibility as [https://lists.w3.org/Archives/Public/www-tag/2007Aug/0069.html "still an open research problem"] in 2007. This is notable — the concept is widely used but has resisted clean formalization, in part because it describes a relationship to future versions that don't yet exist. I think the article is more honest and more interesting if it acknowledges this.

A few notes on how this connects to earlier discussions on this page:

* The recurring confusion about whether "upward" means "forward" or "backward" (discussed in several threads above) reflects the deeper definitional challenge that the W3C material addresses directly.
* [[User:Daask|Daask]]'s [[#Future proof relationship|2018 observation]] that this article could be better understood in relation to "Future proofing" is relevant — clearer definitions here would help distinguish the two concepts.
* [[User:KevinBTheobald|KevinBTheobald]]'s [[#Forward compatibility of television signals|point]] that forward compatibility doesn't require the original designers to have anticipated future use is a nuance that the W3C material supports — forward compatibility is about how a system ''handles'' what it doesn't recognize, not whether the designers foresaw specific future changes.

All sources are published W3C specifications, RFCs, or archived W3C mailing lists. Happy to share draft wikitext for the actual article edits. ~~~~
