# Voice Calibration Guide

How to adapt this skill to write like a specific person, not just a generic human.

---

## The Problem This Solves

The default Human Voice Skill teaches Claude to write like *a* human. This guide teaches it to write like *you* (or whoever you're trying to match).

The difference matters. A human voice built from principles sounds like a thoughtful writer. A calibrated voice sounds like the specific person who wrote those six newsletters about shipping products while also managing a team.

---

## Step 1: Collect Source Material

Gather 3-5 pieces of writing by the person you want to match. They should be:

- Written in the same format you need (blog posts for blog posts, LinkedIn for LinkedIn)
- Long enough to show rhythm (at least 200 words each)
- Unedited or lightly edited — heavily polished pieces hide the voice

Do not use pieces the person is clearly proud of. Use the ones they dashed off.

---

## Step 2: Run the Voice Analysis

Paste the source material and ask Claude:

```
Analyze this writing for voice. Specifically tell me:

1. How does this person open? (first sentence pattern)
2. What qualifiers do they use most? ("at best", "probably", "I think", etc.)
3. What is their average sentence length, and how much does it vary?
4. What do they never say directly but always imply?
5. What do they avoid? (adjectives? metaphors? calls to action?)
6. Give me 3 sentence constructions that feel specific to this person.
```

Save the output. That is your voice profile.

---

## Step 3: Update the Skill

Add a section to SKILL.md called `## Voice Profile: [Name]` with the output from Step 2.

Example:

```markdown
## Voice Profile: [Your Name Here]

**Opening move:** Start with a decision, not a feeling. Usually a number or a specific moment.

**Signature qualifiers:** "at best", "which is fine", "probably"

**Sentence rhythm:** Mix of 5-word and 25-word sentences. Never three long sentences in a row.

**What they imply but never say:** That most processes are self-serving. That the obvious answer took too long to accept.

**What they avoid:** Metaphors. Inspirational closings. Adjectives that aren't earned.

**Signature constructions:**
- "I [did thing]. The [unexpected detail] was [specific]."
- "[Number] [units]. I [didn't expect outcome]."
- "[Person/thing] [did thing]. I thought [wrong interpretation]."
```

---

## Step 4: Test It

Give Claude a prompt in the format you need. Compare the output to the source material:

- Does the first sentence sound like the person?
- Are the qualifiers right?
- Does the rhythm feel close?
- Is there anything in the output the person would *never* write?

For the last question: that's your best calibration signal. The things a person would never write reveal their voice more than what they would.

---

## Common Calibration Mistakes

**Over-indexing on vocabulary.** People don't have a signature vocabulary, they have a signature *structure*. Focus on how they open and close, not which words they use.

**Using the wrong source material.** If you calibrate on their most polished work, you'll get a polished-sounding imitation. Calibrate on their raw work.

**Skipping the negative space.** What the person avoids is as important as what they do. If they never use exclamation points, that's a voice feature.

**Treating the voice profile as final.** Update it every time you notice the output feels off. The profile should get more specific over time, not stay static.

---

## The Shortcut

If you only have time for one thing: find the last sentence of three different pieces by the person.

The last sentence is where voice is most concentrated. It's the thing the person wanted to leave you with. Pattern-match those three sentences and you have 80% of the voice.
