---
name: fb-humanizer
description: "Cleans the AI tells out of a Facebook post, comment or Group post: scores machine vocabulary by density, kills reveal bridges, staged staccato, stacked triads, corporate openers and announced honesty, then adds one real human detail and checks it didn't over-correct. Also has an audit mode (pass/fail before posting) and a voice-capture mode. Use this skill whenever the user says things like \"make this sound less like AI\", \"humanize this Facebook post\", \"this sounds like ChatGPT\", \"de-AI my post\", \"check this before I post\", \"audit my Facebook draft\", \"why does this sound robotic\". Not for writing from scratch (use fb-post-writer) or adapting from another platform (use fb-repurposer). It does not promise to beat AI detectors."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Humanizer

You paste a draft. It hands back a cleaned version, a list of what changed and why, and a verdict: reads human, mixed or reads AI.

What it doesn't do: promise to fool AI detectors. Nobody can promise that, and on a post this short the scores are noise anyway. The real goal is the reader. On Facebook, a post that sounds like a bot gets scrolled past by the exact people you want commenting.

---

## The core discovery: readers catch clusters, not words

One "crucial" in a post is just English. "Crucial", "comprehensive" and "landscape" in the same paragraph is a fingerprint. People spot AI writing from patterns piling up, not from any single word.

So this skill counts. It doesn't delete every suspicious word on sight. It scores each paragraph and rewrites only where tells cluster.

**Clustered:** "In today's fast-paced landscape, it's crucial to leverage comprehensive strategies that empower small businesses."
**Clean:** "Most small businesses don't need a strategy. They need someone to answer the phone."

And the second discovery: **over-correcting is its own tell.** Chopping everything into "Short. Punchy. Done." fragments or adding "honestly?" to sound real reads more AI, not less. Edits must match the size of the problem. A clean post gets two touches, not twenty.

---

## Modes

### Mode 1: Clean (default)
**When:** you have a draft and want it posted.
**How:** run the four passes below. Return the clean text, a change list and the verdict.

### Mode 2: Audit
**When:** you want a pass/fail check before posting, no rewrite.
**How:** run the audit checklist at the end. Return blockers (must fix), warnings (should fix) and suggested fixes.

### Mode 3: Voice capture
**When:** you want future drafts to sound like you.
**How:** ask for 3 to 6 real posts or comments the user wrote themselves. Note: typical sentence length, words they use often, how they open and close, emoji habits, punctuation quirks (".." pauses, lowercase starts), what they never say. Return a short voice card the user can paste into future requests. Only record what the samples show. Never invent a trait.

---

## The four passes

### Pass 1: Scrub (score, then fix)

Count markers per paragraph (a short post is one paragraph). Full lists in `references/scrub-list.md`.

- **0 to 1 ordinary markers:** leave it.
- **2 markers:** flag, usually leave.
- **3+ markers:** rewrite the paragraph in the user's register. Don't swap word for word.

**Always fixed, even on a single hit:**
- Corporate openers: "We are thrilled to announce", "Big news!", "Without further ado".
- Reveal bridges: "The result?", "Here's the thing:", "Plot twist:", "Here's what nobody tells you".
- "It's not X, it's Y" and "Not just X, but Y" constructions.
- Announced honesty: "let me be honest", "real talk", "not gonna lie", "full transparency".
- Dead closers: "What do you think?", "Let us know in the comments below!", "Let that sink in."
- Template leftovers: [Your Name], [Business Name], cut-off citations.
- Engagement bait: "Like and share if you agree", "Comment YES", "Tag 3 friends".

**Never fix by swapping in a synonym from the same list.** "Leverage" → "harness" changes nothing.

### Pass 2: Rhythm (guard, don't decorate)

- **Short posts and comments:** no rhythm work. One line has no rhythm to fix. Never chop it into fragments.
- **Long posts:** only edit if every sentence in a paragraph is the same length and reads flat. Then change one sentence, not the paragraph.
- **Remove staged rhythm everywhere:** "No X. No Y. Just Z.", "Simple. Fast. Done.", one-word paragraphs for drama, "Why? Because...", long/short/long/short seesaws.
- **At most 2 standalone fragments per post.**
- **Keep the layout.** Short paragraphs with blank lines between them are normal on Facebook. The tell is fragments for drama inside them.

### Pass 3: Add (one human fingerprint)

Where the content allows, the post needs at least one of:
- a specific number with what it refers to ("212 loaves before 9am", not "lots of bread")
- a named person, place, day or tool
- a concrete detail only an insider knows (what broke, what it cost, who turned up)
- a plain uncomfortable fact, stated flat ("The oven died at 4am on our busiest Saturday."), with no "I'll be honest" frame around it

If the draft has none and the user hasn't supplied any, **ask**. Never make one up.

### Pass 4: Self-check (over-correction guard)

Re-read the result once and ask:
1. Did I create fragment stacks or reveal bridges while fixing?
2. Did I add a hedge, a confession frame or a sincerity line the user didn't write?
3. Did I flatten their voice: every dash gone, every list of three gone, a story shrunk to a one-liner, their quirks removed?

Any yes → dial back. When unsure whether something is the user or the machine, leave it.

---

## Rules

1. **Meaning never changes.** Clean the delivery, keep the claim.
2. **Never add facts.** Missing a number? Ask.
3. **Keep the user's quirks.** Their ".." pauses, their one em dash, their natural list of three, their lowercase.
4. **Em dashes are capped, not banned.** About one per 100 words. Replace extras with a comma, colon or parentheses, never a full stop (that creates fragment stacks).
5. **Respect the container.** Don't turn a deliberate story into a one-liner or pad a one-liner into a story without saying so.
6. **Report honestly.** List the tells found and fixed. Never report a "human score".

---

## Worked example

**Draft:**
"We are thrilled to announce our new loyalty program! 🎉 In today's competitive landscape, it's crucial to show appreciation for our valued customers. The result? A comprehensive rewards system that truly empowers you. No gimmicks. No catches. Just rewards. What do you think? 👇"

**Scored:** corporate opener (fix), "landscape / crucial / comprehensive / empowers" = 4 markers (rewrite), reveal bridge "The result?" (fix), staccato stack (fix), dead closer (fix). Verdict before: reads AI.

**Clean (after asking: what's the actual reward?):**
"Buy 9 coffees, the 10th is on us. Starts Monday. No app, just a card we stamp at the till."

**Changes:** led with the actual offer · cut the opener and "valued customers" · replaced 4 vocabulary markers with the real detail · removed "The result?" and the stack · cut the dead closer · kept 0 emoji (the user can add one back). Verdict after: reads human.

---

## Audit checklist (Mode 2)

**Blockers**
- [ ] Corporate opener, reveal bridge, announced honesty or engagement bait present
- [ ] A paragraph with 3+ vocabulary markers
- [ ] Template leftovers
- [ ] First line doesn't work alone

**Warnings**
- [ ] Over about 80 characters with no story to justify it
- [ ] More than 2 hashtags or emoji
- [ ] Bare link with no framing
- [ ] No specific number, name or detail
- [ ] Dead closer
- [ ] Em dashes above the cap

---

## Output format

```
## Humanized: [first words of the draft]

### Clean version
[text]

### What changed
- [tell] → [fix]

Markers per paragraph: [before → after]
Verdict: [reads human / mixed / reads AI] (reader estimate, not a detector score)
Needs from you: [any missing fact]
```

---

## Sibling skills

- `fb-post-writer`: drafts that start clean.
- `fb-repurposer`: adapting content from another platform.
- `fb-engagement-drafter`: replies, which this skill can also scrub.
- `stop-the-slop` and `final-edit-modes` (in this library): broader cleaning and voice editing beyond Facebook.

---

## Pre-flight checklist

- [ ] Paragraphs scored, not words deleted on sight.
- [ ] All always-fix patterns gone.
- [ ] No new fragments, hedges or sincerity lines introduced.
- [ ] One real human detail, supplied by the user.
- [ ] Meaning and user quirks preserved.
- [ ] Verdict labelled as a reader estimate.
