# human-voice-skill

A Claude skill that makes AI write like a human who actually lived through the thing.

---

## The Problem

You can feel it when AI wrote something.

Not because of the words. Because of what's missing. The specific number that's slightly too round. The sentence that resolves a little too cleanly. The admission that arrives exactly where you'd expect it to.

AI writes like someone explaining a thing. Humans write like someone who survived it.

This skill is the difference.

---

## What It Does

This skill teaches Claude to write with:

- **Specific numbers** over estimated ones (23 unfinished repos, not "many")
- **Buried admissions** that arrive without announcement
- **Rhythm variance** — short sentences after long ones, not uniform cadence
- **Earned abstractions** — the concept comes after the specific moment that created it
- **No throat-clearing** — the first sentence is almost always deleted

It works for blog posts, LinkedIn posts, READMEs, documentation, changelogs, and release notes. Anywhere developers write and sound like they didn't.

---

## Quick Start

1. Copy the contents of `SKILL.md` into your Claude project instructions (or `.claude/` directory)
2. Give Claude a writing prompt
3. Compare the output to the examples in `examples/`

To calibrate for your specific voice, follow the guide in `philosophy/voice-calibration.md`.

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

## Why This Exists

The skill ecosystem has design skills, coding skills, and productivity skills. Nothing for the thing developers do every day: write.

Not just technical writing. The blog post about the thing you shipped. The LinkedIn post about the thing you learned. The README that makes someone trust the project before they've run a single command.

Those all require a voice. This skill gives you one.

---

## The Source Material

This skill was built from a single article — one that readers described as "the most human thing I've read from an AI session." The writing patterns in SKILL.md were pulled directly from that piece: the specific numbers, the buried self-awareness, the short sentence that lands after a long one.

The skill is the analysis of what made that piece work.

---

## Contributing

Fork it. Adapt the voice calibration guide for your own voice. Open a PR if you find patterns that work that aren't in here yet.

The skill should get more specific over time, not stay generic.

---

## License

MIT. Use it, fork it, build on it.
