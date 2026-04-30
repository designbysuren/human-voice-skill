# Example: Technical Blog Post

**Format:** Developer blog post  
**Prompt type:** Remove a feature nobody wanted  
**Skill rules demonstrated:** 1, 3, 4, 5, 6

---

## The Prompt

```
Write a short blog post about the time we removed a feature that users did not actually want.
Use the human-voice skill.
```

---

## Before (AI Voice)

> When building products, it is important to validate assumptions with users before investing significant development time. Our team recently learned this lesson when we built a progress tracking feature that did not meet user needs. After four months of low engagement, we made the decision to remove the feature and rebuild it based on actual user feedback. This experience reinforced the value of user research and iterative development in the product process.

**What went wrong:**

- Opens with a general principle, not a specific moment
- "Our team recently learned" hides the actual failure behind passive framing
- "Did not meet user needs" is vague. What did users actually do?
- "This experience reinforced the value of" is the AI wisdom-summary tell
- No specific number, no named detail, no self-blame

---

## After (Human Voice)

### We Built the Wrong Thing for a Year

The feature had a progress bar.

We spent two weeks getting the animation right. The fill speed, the color, the little checkmark at the end. It looked good. We were proud of it.

We showed it to three users before launch. None of them wanted to track progress the way we built it. One of them asked if she could turn it off. We thought she was the outlier.

She was not.

Four months after launch, we pulled the feature. Engagement was flat. Support tickets mentioned it twice, both times to ask how to hide it. We had built something technically solid that solved a problem nobody had.

That was not the model's fault. That was not the timeline's fault. I had made assumptions about what "tracking progress" meant and I had never tested them. The progress bar was an answer to a question I had written myself.

We removed it in a single PR. Took about forty minutes.

I still think the animation was good.

---

## Rule Breakdown

| Rule | Where it appears |
|------|-----------------|
| Rule 1: Write from the scar | Opens with "The feature had a progress bar" not "we learned that..." |
| Rule 3: Let one thought be incomplete | "I still think the animation was good" has no payoff |
| Rule 4: Use specific numbers | "three users," "four months," "twice," "forty minutes" |
| Rule 5: Vary sentence length | "She was not." lands after three longer sentences |
| Rule 6: Self-blame once, specifically | "I had made assumptions... a question I had written myself" |

**Signature line:** "The progress bar was an answer to a question I had written myself."

**What was suppressed:** No summary paragraph. No "the lesson here is." No "in conclusion." The final line is incomplete on purpose.
