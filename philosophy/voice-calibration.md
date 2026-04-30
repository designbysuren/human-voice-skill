# Voice Calibration Guide

> Use this when you want Claude to write in a specific person's voice, not just "human-sounding" writing in general. The seven rules in SKILL.md produce credible human writing. This guide produces writing that sounds like *you*.

---

## Why Calibration Matters

The seven rules will produce writing that feels human. But "human" is broad. There is a difference between writing that sounds like a thoughtful developer and writing that sounds like the specific person who wrote those six post-mortems about infrastructure failures while managing a team through a reorg.

Calibration closes that gap.

---

## Step 1: Collect the Right Samples

Ask for 3-5 pieces of writing from the person. Quality of samples matters more than quantity.

**Good sources:**
- LinkedIn posts they wrote quickly, not drafted over days
- Slack messages to the team about something they cared about
- Internal post-mortems or retrospectives
- Personal blog posts on topics they know well

**Avoid:**
- Press releases or formal announcements
- Heavily edited pieces or content with a communications team
- Writing from more than two years ago (voice shifts)

**Minimum length:** 150 words per sample. Shorter than that and you cannot see rhythm.

---

## Step 2: Extract the Five Signals

Read the samples and answer these five questions. Write the answers down before generating anything.

---

### Signal 1: Sentence Rhythm

Count average words per sentence across all samples.

| Average | Signature |
|---------|-----------|
| Under 12 | Short, punchy. Emphatic. Stops hard. |
| 12 to 20 | Mixed. Builds then lands. |
| Over 20 | Long builds. Thinks on the page. |

**Critical:** the signature is not just average length. It is variance. A writer who alternates 5-word and 30-word sentences has a completely different voice than one who writes 15-word sentences consistently. Measure both.

---

### Signal 2: Hedging Style

Does the writer hedge? How?

- **Explicit uncertainty:** "I think," "probably," "I am not sure," "I could be wrong"
- **Earned nuance:** "at best," "under the right conditions," "most of the time"
- **Flat:** states things without qualification and lets the reader decide

Most writers use one of these consistently. Match it. Do not average toward mild hedging if the writer is flat.

---

### Signal 3: Admission Pattern

When the writer admits a mistake or limitation, how do they frame it?

- **Direct:** "I was wrong about this"
- **Framed:** "What I missed was..." or "Looking back..."
- **Implied:** describes the outcome without naming the failure explicitly

This signal is often the hardest to match. If the writer uses implied admissions, an explicit "I was wrong" in your output will feel out of character.

---

### Signal 4: Analogy Density and Style

- How often do analogies appear? (every paragraph / once per piece / rarely)
- Are they elaborate (multi-sentence) or brief (one clause)?
- Announced ("think of it like...") or unannounced?

Writers who use analogies rarely tend to make them count. Writers who use them often tend to make them brief. Do not import your own analogy habits.

---

### Signal 5: Structural Preference

- Headers and bullets, or flowing paragraphs?
- Dense text or lots of white space and short lines?
- Consistent opening move? (quiet observation / bold claim / scene / question)

The opening move is the most consistent signal. If the writer always opens with a quiet observation, do not open with a bold claim. Match the move.

---

## Step 3: Write the Calibration Note

Before generating the output, write a one-paragraph note like this:

> "This writer uses short sentences that spike longer every third or fourth. They hedge with 'probably' and 'if I am being honest' but rarely. They admit mistakes directly and without drama. Analogies are brief, arrive without announcement, appear once per piece. They write in paragraphs, not bullets. They tend to open with a quiet observation."

Write the output against that note.

---

## Step 4: Check Before Delivering

After drafting, read the samples and the output side by side.

Ask one question: if someone who knew this writer read both, would they believe the output came from the same person?

If no, identify which signal is off. Usually it is rhythm or hedging style. Adjust one signal at a time.

---

## Common Calibration Mistakes

**Averaging toward neutral.** If the writer is unusually terse, write tersely. If they are unusually long, write long. The distinctiveness is not a flaw to correct. It is the voice.

**Copying surface features without the underlying logic.** If the writer uses sentence fragments, they use them for emphasis. Find where emphasis belongs in your output and use the fragment there. Do not scatter fragments randomly.

**Ignoring the opening move.** This is the most consistent signal and the easiest to miss. Match it.

**Using the wrong samples.** Heavily edited or formal writing hides the voice. Find the raw stuff.

---

## The Shortcut

If you only have time to extract one signal: find the last sentence of three different pieces.

The last sentence is where voice concentrates. It is the thing the writer wanted to leave you with. Pattern-match those three closing lines and you have 80% of what you need.
