# human-voice-skill

A Claude Code skill that makes AI write like a human who actually lived through the thing.

Not "passes AI detection." Actually credible.

---

## The Problem

AI writing has a signature. Developers and readers recognize it in seconds.

- Every paragraph is the same length
- Every claim is explained right after it is made
- Nothing is ever admitted as a mistake
- Every analogy is introduced as "to illustrate this concept"

You can feel it. It does not matter if the facts are right. The writing feels generated, which means it feels unearned.

This skill fixes that.

---

## What This Skill Does

It teaches Claude seven rules for writing that sounds like a person thought it, doubted it, and then typed it anyway.

The rules are based on a simple observation: what makes writing feel human is not complexity or cleverness. It is texture. Second thoughts. The specific number instead of the vague one. The sentence that does not resolve. The analogy that arrives mid-thought without announcement.

This skill encodes those patterns and suppresses the AI defaults that kill credibility.

---

## Install

**In Claude Code:**

```bash
# Clone into your .claude/skills directory
git clone https://github.com/designbysuren/human-voice-skill ~/.claude/skills/human-voice-skill
```

Claude will automatically detect and use the skill when relevant.

**Manual:**

Copy `SKILL.md` into any `.claude/skills/` directory in your project. Claude Code discovers skills automatically.

---

## Usage

Once installed, reference the skill when asking Claude to write:

```
Write a blog post about why we deprecated our feature flags system. Use the human-voice skill.
```

Or for voice matching:

```
Here are three examples of how I write: [paste samples]
Using the human-voice skill, write a LinkedIn post about our launch.
```

The skill will:

- Extract your rhythm, hedging style, and admission pattern from the samples
- Apply the seven rules
- Suppress the AI writing defaults
- Check the output against the signature lines test before finishing

---

## The Seven Rules (Short Version)

1. **Write from the scar, not the lesson** - Start with the moment you were still wrong
2. **Use the "at best" move** - Hedge in ways that show you thought harder about the claim
3. **Let one thought be incomplete** - Not every tension needs resolution
4. **Use specific numbers** - Three users, not "several users"
5. **Vary sentence length on purpose** - Break the AI rhythm
6. **Self-blame once, specifically** - Not "we failed to validate" but "I built it for myself"
7. **Let analogies arrive late** - No "to illustrate this concept"

Full rules with examples are in `SKILL.md`.

---

## Example

**Before (AI voice):**

"When working with AI tools, it is important to consider the quality of your prompts. Research has shown that clear and specific instructions lead to better outputs. By investing time in crafting thoughtful prompts, teams can significantly improve their results."

**After (human voice):**

"I spent six weeks blaming the model. The outputs were vague, circular, not useful. Then a colleague looked over my shoulder for ten minutes and asked one question: what do you actually want it to do?

I did not have an answer. That was the problem.

At best, a prompt is the packaging of thinking. I had not done the thinking."

---

## Who This Is For

- Developers writing technical blog posts or essays
- Founders writing LinkedIn content or launch posts
- Technical writers who want READMEs that feel authored
- Anyone who has been told "this sounds AI-generated" and did not know how to fix it

---

## Compatibility

Works with Claude Code, Cursor, Windsurf, Opencode, and any agent that supports `.claude/skills/` directories with `SKILL.md` files.

---

## Repo Structure

```
human-voice-skill/
  README.md                    <- you are here
  SKILL.md                     <- the skill Claude reads and uses
  examples/
    blog-post.md               <- before/after with annotations
    linkedin-post.md           <- second format, shows range
  philosophy/
    voice-calibration.md       <- how to match a specific person's voice
```

---

## Contributing

The rules are intentionally opinionated. If you have a pattern that consistently makes AI writing feel more human and is not already covered, open an issue with a before/after example.

Pull requests that add examples for specific writing formats (changelogs, post-mortems, release notes, cold emails) are welcome.

---

## License

MIT
