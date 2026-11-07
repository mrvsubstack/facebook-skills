---
name: fb-hook-extractor
description: "Breaks down why a Facebook post took off: names its shape (from the 10 Facebook post shapes), maps its hook line, body beats and close, explains the comment and share triggers, flags anything you shouldn't copy, and hands back a fill-in template for your own topic. Works from pasted post text plus any visible numbers. Use this skill whenever the user says things like \"why did this Facebook post go viral\", \"break down this post\", \"reverse-engineer this Facebook post\", \"give me a template from this post\", \"what made this get so many shares\", \"analyse my best Facebook post\". Not for writing a post from scratch (use fb-post-writer)."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Hook Extractor

You paste a Facebook post that did well (yours or someone else's), plus its numbers if you can see them. It hands back a teardown: the shape it used, why it worked, what not to copy and a blank template you can fill with your own topic.

Facebook can't be read directly here, so paste the text. Links alone won't do.

---

## The core discovery: copy the mechanism, never the words

A viral post works because of a mechanism: an easy question, a number that reframes something, a story that turns. The words are just that mechanism wearing one creator's clothes.

People who copy the words get a pale imitation. People who copy the mechanism get a new post that works for the same reason.

**Copied words:** "My grandma's bread recipe has 3 ingredients and changed my life." → "My grandma's budget spreadsheet has 3 columns and changed my life."
**Copied mechanism (small number + personal heirloom + easy share):** "The best money advice I ever got fits on a Post-it. My dad wrote it in 1994."

The second keeps what worked: a small, concrete thing with a person behind it. And it's yours.

---

## Intake

1. **The post text**, word for word.
2. **The numbers** if visible: reactions, comments, shares, rough age of the post.
3. **The account type and size**, roughly (a 2 million follower Page is a different game from a 900 follower one).
4. **Your topic**, so the template can be mapped to it.

If numbers are missing, say the analysis is based on structure only.

---

## The 10 shapes (from fb-post-writer)

| Code | Shape | Tell-tale features | Usual goal |
|---|---|---|---|
| F1 | One-Line Opinion | Flat, unhedged take | Shares |
| F2 | Small Number | Built around one concrete number | Shares |
| F3 | Easy Question | The whole post is a low-effort question | Comments |
| F4 | This or That | A binary choice | Comments |
| F5 | Relatable Moment | A shared feeling, no setup | Reactions |
| F6 | Behind the Scenes | A real glimpse inside | Reactions |
| F7 | Useful Tip | One action you can take today | Shares |
| F8 | Story With a Turn | Opens at tension, turns, quotable ending | Shares + comments |
| F9 | Human Announcement | News led plainly, not corporately | Shares |
| F10 | Spotlight | A named person + an invitation | Shares + comments |

---

## Steps

1. **Container.** Short (one or two lines, no "See more") or long (a fold, several paragraphs)?
2. **Classify.** Match features to shapes. If two fit, give both with a rough split ("70% F8, 30% F10") and say which drove the result.
3. **Map the structure.**
   - **Hook line:** the words above the fold and why they earn the tap.
   - **Beats:** for long posts, label each paragraph (tension, detail, turn, lesson).
   - **Close:** the line that triggers the share or the comment.
4. **Name the triggers.** What made people act:
   - identity (sharing says something about the sharer)
   - usefulness (passing on a tip)
   - low-effort answer (anyone can reply in three words)
   - disagreement (a fair fight with two sides)
   - emotion (pride, nostalgia, outrage, laughter)
   - a named person or place people know
5. **Read the numbers.** High shares vs comments vs reactions tell you which goal it actually hit. Many shares with few comments = identity or usefulness. Many comments with few shares = question or debate.
6. **Flag what not to copy:** engagement bait ("tag a friend who..."), corporate openers, stacks of hashtags, outrage that only works for that creator, claims you can't verify, and stolen or unattributed content.
7. **Build the template** with `{slots}`, keeping the mechanism intact.
8. **Fill it once** with the user's topic as a starting draft.

---

## Rules

1. **Explain the mechanism in one sentence before anything else.**
   - Bad → "This post is engaging because it connects with the audience."
   - Good → "It asks a question anyone can answer with one word, and the answer says something about who they are."
2. **Separate the post from the poster.** A huge Page can post anything and get reach. Note when the account size, not the post, did the work.
3. **Never claim to know the algorithm.** Say what the structure suggests, not what Facebook "decided".
4. **The template keeps the length.** A 60-character post becomes a 60-character template, not a paragraph.
5. **Never reproduce the original as your draft.** The filled example must be a new post.

---

## Worked example

**Post pasted:** "Name a food you loved as a kid that you'd still eat today. I'll start: Angel Delight." (illustrative example: a UK nostalgia Page; 4.1K comments, 300 shares)

**Teardown:**
- **Shape:** F3 Easy Question (90%), with an F5 nostalgia layer.
- **Mechanism:** a question everyone can answer from memory in two words, with the poster's own answer to show the format and lower the barrier.
- **Hook:** the whole post. Under 90 characters, no fold.
- **Triggers:** low-effort answer + nostalgia + identity (your answer dates you).
- **Numbers:** comments far above shares = it hit the comment goal, as designed.
- **Don't copy:** nothing risky here. The "I'll start" line is the clever part. Keep it.

**Template:** `Name a {category} you {past experience} that you'd still {action} today. I'll start: {your own answer}.`

**Filled for a bookkeeping Page:** "Name a money habit you learned as a kid that you still use today. I'll start: the coin jar."

---

## Output format

```
## Teardown: "[first line of the post]"

Shape: [code + name] ([confidence])
Mechanism (one sentence): [ ]
Container: [short / long]

Structure
- Hook: [ ]
- Beats: [ ]
- Close: [ ]

Triggers: [list]
What the numbers say: [ ] (or "structure only, no numbers given")
Don't copy: [list]

Template: [with {slots}]
Your version: [filled draft]
```

---

## Sibling skills

- `fb-post-writer`: turn the template into finished options.
- `fb-humanizer`: scrub your filled version before posting.
- `fb-content-planner`: slot the shape into your week.
- `fb-repurposer`: when the post you admire is on another platform.

---

## Pre-flight checklist

- [ ] Mechanism stated in one sentence.
- [ ] Shape named with confidence. Second shape noted if it fits.
- [ ] Hook, beats and close mapped.
- [ ] Numbers read, or the gap stated.
- [ ] Risky elements flagged.
- [ ] Template keeps the original's length and mechanism.
- [ ] Filled example is new, not a copy.
