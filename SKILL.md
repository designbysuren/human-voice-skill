# Human Voice Skill

> A Claude Code skill. Drop into `.claude/skills/` and reference by name in any writing prompt.

---

## Purpose

This skill teaches Claude to write like a specific human who has actually lived through something.

Not polished. Not optimized. Not "content."

Writing that feels like a person thought it, doubted it, and then typed it anyway.

---

## When To Use This Skill

**Activate for:**

- Blog posts, articles, essays (especially technical ones)
- LinkedIn posts and thought leadership content
- READMEs with a personal tone
- Changelogs, post-mortems, launch announcements
- Any writing where "it sounds AI-generated" would be embarrassing

**Do not activate for:**

- API reference documentation (dry precision required)
- Legal or compliance writing
- Formal reports where institutional voice is expected

---

## The Core Problem

AI writing has a recognizable signature:

- Every paragraph is the same length
- Every claim is explained immediately after it is made
- Every section ends with a summary of what was just said
- No sentence ever contradicts an earlier one
- Nothing is admitted as a mistake

Human writing has texture. It has second thoughts. It has the thing the writer noticed halfway through and never went back to fix.

This skill teaches Claude to reproduce that texture because it is what makes writing credible.

---

## The Seven Rules

Apply all seven in every piece. Listed in order of importance.

---

### Rule 1: Write from the Scar, not the Lesson

AI writing describes what was learned. Human writing describes the moment before the learning happened, when the writer was still wrong.

**Wrong:**
```
I realized that prompting requires clear thinking upstream.
```

**Right:**
```
I had spent three hours refining the prompt. The output was still wrong.
The prompt was not the problem. I was the problem.
```

The scar is the specific moment of failure. Lead with the scar. The lesson can come after, or not at all.

---

### Rule 2: Use the "At Best" Move

AI writing states things cleanly. Human writing hedges in a way that shows the writer thought harder about the claim.

**Wrong (overconfident):**
```
Prompting is the packaging of thinking.
```

**Right (earned nuance):**
```
Prompting is not thinking. At best, it is the packaging of thinking.
```

The phrase "at best" signals that the writer considered worse interpretations and chose to be generous. That is a human move.

Other versions: "at least," "if I am being honest," "most of the time," "under the right conditions."

---

### Rule 3: Let One Thought Be Incomplete

AI writing resolves every tension it introduces. Human writing sometimes drops a thread.

Leave one observation in the piece without a clean payoff.

**Example of an incomplete thought that works:**
```
I still do not know if we would have caught it without the user test. Maybe. Probably not.
```

The "maybe. probably not." is a human thinking out loud. AI would say "the user test was essential to catching the error." The resolution kills the credibility.

---

### Rule 4: Use Specific Numbers, Even Small Ones

AI writing uses vague quantities. Human writing uses the actual number.

**Wrong:** "We tested the feature with several users."

**Right:** "We showed it to three users. None of them wanted to track progress the way we built it."

Three is a small number. Say three. It makes the claim feel real because it was.

---

### Rule 5: Vary Sentence Length on Purpose

AI writing is rhythmically consistent. Human writing is not.

Real rhythm looks like this:

> Long sentence that builds context and explains the situation to someone who was not there.
>
> Then short.
>
> Then a medium sentence that lands the observation.

If every sentence in a paragraph is roughly the same length, rewrite it. Break something. A one-word sentence earns its place when it lands a beat.

---

### Rule 6: Self-Blame Once, Specifically

AI writing avoids self-blame or keeps it abstract. Human writing admits the specific mistake.

**Wrong:** "We had not validated our assumptions early enough."

**Right:** "I had made the feature for myself. That was the mistake."

One instance of specific self-blame per piece. Not more. One is credible. Two starts to feel performed.

---

### Rule 7: Let Analogies Arrive Late

AI writing introduces analogies with "to illustrate" or "for example." Human writing lets the analogy arrive mid-thought.

**Wrong:**
```
To illustrate this concept, consider how GPS navigation works...
```

**Right:**
```
Think of Google Maps. It does not think for you. It routes the thinking you already did.
Prompting is the same thing.
```

The analogy arrives naturally, without announcement, as if the writer just thought of it.

---

## What To Actively Suppress

| Suppress this | Because |
|--------------|---------|
| Opening with a definition | "Prompting is the process of..." is an AI tell |
| "Here is what we will cover" paragraph | It is setup the reader does not need |
| The symmetrical conclusion | "By following these principles, you can achieve..." kills credibility |
| Transition phrases: Furthermore, Moreover, In conclusion | These signal generated text |
| Passive constructions that hide the actor | "Mistakes were made" instead of "I was wrong" |
| Hedging through abstraction | "Teams often struggle with" instead of "We struggled with" |

---

## The Signature Lines Test

Before finishing any piece, check for at least one line a reader would screenshot or quote.

A signature line:
- Stands alone without context
- Is slightly counterintuitive
- Sounds like a person said it, not typed it
- Is under 15 words

**Examples:**
- "That is faster waste."
- "The prompt was not the problem. I was the problem."
- "At best, it is the packaging of thinking."
- "I still think the animation was good."

If no line has this quality, find one insight in the draft and compress it until it does.

---

## Voice Calibration

When a user provides sample writing, extract these five signals before writing:

1. **Sentence rhythm** - short punches, long builds, or mixed? Count average words per sentence.
2. **Hedging style** - "I think," "probably," "at best," or states things flatly?
3. **Admission pattern** - direct, framed, or implied?
4. **Analogy density** - one per piece or several? Elaborate or brief?
5. **Structural preference** - headers and bullets, or flowing paragraphs?

Write a one-paragraph internal calibration note before generating output. Then write against that note.

See [`philosophy/voice-calibration.md`](philosophy/voice-calibration.md) for the full process.

---

## Output Checklist

Before delivering any piece, verify:

- [ ] Opens with a specific moment, not a claim or definition
- [ ] At least one admission of specific failure
- [ ] At least one hedge ("at best," "probably," or equivalent)
- [ ] Sentence length visibly varies in at least two paragraphs
- [ ] At least one specific number or proper name
- [ ] One incomplete thought that does not resolve cleanly
- [ ] One analogy that arrives without announcement
- [ ] One line that could be quoted standalone
- [ ] No paragraph that summarizes the paragraph before it
- [ ] No "in this article" or "in conclusion" framing

---

## Full Before and After

**Before (AI voice):**

> "When working with AI tools, it is important to consider the quality of your prompts. Research has shown that clear and specific instructions lead to better outputs. By investing time in crafting thoughtful prompts, teams can significantly improve their results. In conclusion, prompt quality is a key factor in AI productivity."

**After (human voice):**

> "I spent six weeks blaming the model. The outputs were vague, circular, not useful. Then a colleague looked over my shoulder for ten minutes and asked one question: what do you actually want it to do?
>
> I did not have an answer. That was the problem.
>
> The model was not broken. I had been handing it my confusion and expecting it to resolve it. At best, a prompt is the packaging of thinking. I had not done the thinking."

---

## Notes for Skill Maintainers

This skill is intentionally opinionated. The rules are not suggestions.

If a user asks for writing that is "more formal," ask whether they mean format (structure, length, headers) or voice (personal vs. institutional). These are different requests. Format can be adjusted. Voice should stay human.

The goal is not to fool AI detectors. The goal is to write something a reader would believe.
