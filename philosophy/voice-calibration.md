# Voice Calibration Guide

Use this when a user wants Claude to write in their specific voice, not just "human-sounding" writing.

---

## Step 1: Request Samples

Ask for 3-5 examples of the person's actual writing. The best samples are:

- Written under mild time pressure (not heavily edited)
- On a topic the person cares about
- At least 150 words each

LinkedIn posts, Slack messages to the team, internal post-mortems, and personal blog posts all work well. Press releases and formal reports do not.

---

## Step 2: Extract the Five Signals

Read the samples and answer these five questions:

### Signal 1: Sentence Rhythm

Count the average words per sentence across the samples. Is it under 12 (short, punchy), 12-20 (mixed), or over 20 (long builds)?

Note: the rhythm signature is not just average length. It is the variance. A writer who alternates between 5-word and 30-word sentences has a different signature than one who writes 15-word sentences consistently.

### Signal 2: Hedging Style

Does the writer hedge? If so, how?

- Explicit uncertainty: "I think," "probably," "I am not sure"
- Earned nuance: "at best," "under the right conditions," "most of the time"
- No hedging: states things flatly and lets the reader decide

### Signal 3: Admission Pattern

When the writer admits a mistake or limitation, how do they do it?

- Direct: "I was wrong about this"
- Framed: "What I missed was..."
- Implied: describes the failure without naming it as one

### Signal 4: Analogy Density and Style

- How often do analogies appear? (every paragraph, once per piece, rarely)
- Are they elaborate (multi-sentence) or brief (one clause)?
- Do they come with announcement ("think of it like...") or without?

### Signal 5: Structural Preference

- Headers and bullet points, or flowing paragraphs?
- Does the writer use line breaks as rhythm (short lines, lots of space) or dense blocks?
- Is there a consistent opening move? (question, scene, bold claim, quiet observation)

---

## Step 3: Write the Calibration Note

Before generating the output, write a one-paragraph internal note like this:

"This writer uses short sentences that spike longer every third or fourth. They hedge with 'probably' and 'I think' but rarely. They admit mistakes directly and without drama. Analogies are brief, arrive without announcement, appear once per piece. They write in paragraphs, not bullets. They tend to open with a quiet observation rather than a bold claim."

Then write the output against that note.

---

## Step 4: Check Before Delivering

After drafting, re-read the samples and the output side by side.

Ask: if someone who knew this writer read both, would they believe the output came from the same person?

If not, identify which signal is off and adjust. Usually it is rhythm or hedging style.

---

## Common Calibration Mistakes

**Averaging toward neutral.** If the writer is unusually terse, write tersely. Do not smooth it out. The distinctiveness is the point.

**Copying surface features without the underlying logic.** If the writer uses fragments, it is not random. They use fragments for emphasis. Find where emphasis belongs in your output and use the fragment there, not elsewhere.

**Ignoring the opening move.** How a writer starts a piece is usually their most consistent signature. Match it.
