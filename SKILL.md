# Human Voice Skill

## What This Skill Does

This skill teaches Claude to write like a specific human who has actually lived through something.

Not polished. Not optimized. Not "content."

Writing that feels like a person thought it, doubted it, and then typed it anyway.

---

## When To Use This Skill

Trigger this skill when the user asks for:

- Blog posts, articles, or essays (especially technical ones)
- LinkedIn posts or thought leadership content
- README files with a personal tone
- Changelogs that sound human
- Any writing where "it sounds AI-generated" would be embarrassing

**Do NOT use this skill for:**

- API documentation that needs to be dry and precise
- Legal or compliance writing
- Formal reports where personal voice is inappropriate

---

## The Core Problem This Solves

AI writing has a signature. Developers and readers recognize it instantly.

The signature looks like this:

- Every paragraph is the same length
- Every claim is explained immediately after it is made
- Every section ends with a summary of what was just said
- No sentence ever contradicts an earlier one
- Nothing is admitted as a mistake

Human writing does the opposite. It has texture. It has second thoughts. It has the thing the writer noticed halfway through and never went back to fix.

This skill teaches Claude to reproduce that texture, not as decoration, but because it is what makes writing credible.

---

## The Seven Rules

Apply all seven in every piece of writing. They are listed in order of importance.

### Rule 1: Write from the scar, not the lesson

AI writing describes what was learned. Human writing describes the moment before the learning happened, when the writer was still wrong.

**Bad:**

"I realized that prompting requires clear thinking upstream."

**Good:**

"I had spent three hours refining the prompt. The output was still wrong. The prompt was not the problem. I was the problem."

The scar is the specific moment of failure. Lead with the scar. The lesson can come after, or not at all.

### Rule 2: Use the "at best" move

AI writing states things cleanly. Human writing hedges in a way that shows the writer has thought harder about the claim.

**Overconfident (AI-sounding):**

"Prompting is the packaging of thinking."

**Human (with earned nuance):**

"Prompting is not thinking. At best, it is the packaging of thinking."

The phrase "at best" signals that the writer considered worse interpretations and chose to be generous. That is a human move.

Other versions of this move: "at least," "if I am being honest," "most of the time," "under the right conditions."

### Rule 3: Let the thought be incomplete once

AI writing resolves every tension it introduces. Human writing sometimes drops a thread because the writer realized mid-sentence they did not know how to finish it.

This does not mean write badly. It means leave one observation in the piece that does not have a clean payoff.

Example of an incomplete thought that works:

"I still do not know if we would have caught it without the user test. Maybe. Probably not."

That "maybe. probably not." is a human thinking out loud. AI would have said "the user test was essential to catching the error." The resolution kills the credibility.

### Rule 4: Use specific numbers and names, even small ones

AI writing uses vague quantities. Human writing uses the actual number, even when it is embarrassingly small.

**AI:** "We tested the feature with several users."

**Human:** "We showed it to three users. None of them wanted to track progress the way we built it."

Three is a small number. Say three. It makes the claim feel real because it was.

### Rule 5: Vary sentence length on purpose

AI writing is consistent. Human writing is not. Real rhythm looks like this:

Long sentence that builds context and explains the situation to someone who was not there.

Then short.

Then a medium sentence that lands the observation.

That's it.

If every sentence in a paragraph is roughly the same length, rewrite the paragraph. Break something. Add a one-word sentence if it earns it.

### Rule 6: Self-blame once, specifically

AI writing avoids self-blame or keeps it abstract. Human writing admits the specific mistake, not a category of mistake.

**Abstract (AI):** "We had not validated our assumptions early enough."

**Specific (human):** "I had made the feature for myself. That was the mistake."

One instance of specific self-blame per piece. Not more. One is credible. Two starts to feel performed.

### Rule 7: Let the analogy arrive late

AI writing introduces analogies as "examples" or "to illustrate." Human writing lets the analogy arrive in the middle of a thought, as if the writer just thought of it.

**AI:** "To illustrate this concept, consider how GPS navigation works..."

**Human:** "Think of Google Maps. It does not think for you. It routes the thinking you already did. Prompting is the same thing."

The analogy arrives naturally, without announcement. It feels like the writer found it mid-thought.

---

## Voice Calibration: How To Capture a Specific Person's Voice

When a user provides sample writing, extract these five signals before writing:

1. **Sentence rhythm signature** - does the writer use short punches, long builds, or mixed? Count the average words per sentence in the sample.
2. **Hedging style** - do they say "I think," "probably," "at best," or do they state things flatly?
3. **Admission pattern** - do they admit mistakes directly, or through implication?
4. **Analogy density** - one per piece, or several? Elaborate or brief?
5. **Structural preference** - do they use headers and lists, or do they write in paragraphs?

Reproduce all five in the output. Do not average toward generic. The specificity is the point.

See `philosophy/voice-calibration.md` for the full calibration process.

---

## What To Actively Suppress

When writing with this skill active, suppress the following instincts:

**Suppress: opening with a definition**
"Prompting is the process of providing instructions to an AI..."

**Suppress: the "here is what we will cover" paragraph**
"In this article, we will explore three key lessons from..."

**Suppress: the symmetrical conclusion**
"By following these principles, you can achieve..."

**Suppress: transition phrases that signal AI**
"Furthermore," "Moreover," "It is worth noting that," "In conclusion"

**Suppress: passive constructions that hide the actor**
"Mistakes were made" instead of "I was wrong"

**Suppress: hedging through abstraction**
"Teams often struggle with" instead of "We struggled with"

---

## The Signature Lines Test

Before finishing any piece, check if it contains at least one line a reader would screenshot or quote.

Signature lines have these properties:

- They can stand alone without context
- They are slightly counterintuitive
- They sound like a person said them, not typed them
- They are under 15 words

Examples of signature lines:

- "That is faster waste."
- "The prompt was not the problem. I was the problem."
- "I had made myself worse."
- "At best, it is the packaging of thinking."

If the piece has no line with this quality, find one insight in the draft and compress it until it does.

---

## Quick Reference Checklist

Before delivering any output, verify:

- [ ] Opening with a specific moment, not a claim
- [ ] At least one admission of specific failure
- [ ] At least one hedge using "at best," "probably," or equivalent
- [ ] Sentence length varies visibly in at least two paragraphs
- [ ] At least one specific number or name
- [ ] One incomplete thought that does not resolve cleanly
- [ ] One analogy that arrives without announcement
- [ ] One line that could be quoted standalone
- [ ] No paragraph that summarizes what the previous paragraph just said
- [ ] No opening with a definition or "in this article" framing

---

## Example: Before and After

**Before (AI voice):**

"When working with AI tools, it is important to consider the quality of your prompts. Research has shown that clear and specific instructions lead to better outputs. By investing time in crafting thoughtful prompts, teams can significantly improve their results. In conclusion, prompt quality is a key factor in AI productivity."

**After (human voice):**

"I spent six weeks blaming the model. The outputs were vague, circular, not useful. Then a colleague looked over my shoulder for ten minutes and asked one question: what do you actually want it to do?

I did not have an answer. That was the problem.

The model was not broken. I had been handing it my confusion and expecting it to resolve it. At best, a prompt is the packaging of thinking. I had not done the thinking."

---

## Notes For Skill Maintainers

This skill is intentionally opinionated. The rules are not suggestions.

If a user asks for writing that is "more formal" or "more professional," ask them whether they mean format (structure, length, use of headers) or voice (personal vs. institutional). These are different requests. Format can be adjusted. Voice should stay human.

The goal is not to fool AI detectors. The goal is to write something a reader would believe.
