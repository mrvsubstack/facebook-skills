---
name: fb-repurposer
description: "Rebuilds content you already made (a LinkedIn post, X thread, blog, newsletter, YouTube script or Instagram caption) as a native Facebook post for a Page, profile or Group. Finds the one idea worth keeping, picks a Facebook post shape, warms the tone, puts the whole point above the See more fold, handles links and strips off-platform clutter. Use this skill whenever the user says things like \"turn this into a Facebook post\", \"repurpose my LinkedIn post for Facebook\", \"adapt my newsletter for my Facebook group\", \"post this blog on Facebook\", \"make this work on Facebook\", \"cross-post this to my Page\". Not for writing from a blank page (use fb-post-writer) or cleaning a Facebook draft (use fb-humanizer)."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Repurposer

You paste something you already made and say where on Facebook it's going. It hands back 1 to 3 Facebook-native versions, with a note on what came from where.

It transforms. It doesn't invent.

---

## The core discovery: Facebook is a kitchen table, not a conference stage

Each platform has a room. LinkedIn is a conference: polished, professional, a little performative. X is a bar argument. Instagram is a gallery. Facebook is the kitchen table: friends, neighbours, family, locals, people who've known you for years.

Paste a LinkedIn post onto Facebook and it sounds like a press release read aloud at dinner.

**LinkedIn original:** "Excited to share that after 18 months of strategic planning, our team has successfully launched a scalable client onboarding framework that reduced churn by 22%."
**Facebook rebuild:** "We lost 1 in 5 new clients in their first month. Last year that drove me mad. So we changed how we say hello. Churn's down 22%."

Same fact. Kitchen-table voice.

---

## Intake

1. **The source**, pasted in full.
2. **Destination:** Page, personal profile or a Group (Groups need extra care with promotion rules).
3. **Goal:** shares, comments or reactions.
4. **The audience on that Facebook account** (often different from the source platform's audience: more local, more personal, less industry).
5. **Any link** the post must carry.

---

## Steps

1. **Find the spine.** One claim, one story or one number. Write it in a sentence. Most repurposing fails because it keeps the words instead of the point.
2. **Pick the container.**
   - One claim, number or moment → short post (aim under about 80 characters).
   - A real story or launch → longer story post.
3. **Pick a shape** from `fb-post-writer` (F1 to F10) by goal.
4. **Warm the tone.** Swap industry words for plain ones. Add the human detail the source left out (who, where, what it felt like), but only from what the user tells you.
5. **Put the whole point above the fold.** Line one stands alone.
6. **Handle the link.** Posts with outbound links tend to reach fewer people. Options: the post stands on its own claim with the link in the first comment, or the link stays with strong framing text above it. Tell the user it's a trade-off worth testing.
7. **Strip off-platform clutter** (see table).
8. **Group check.** If it's going to a Group, read the Group's rules (ask the user to paste them). Remove anything that reads as self-promotion unless the rules allow it. Lead with the question or lesson, not your offer.
9. **Scrub.** Run the `fb-humanizer` rules: no corporate openers, no reveal bridges, no staged rhythm.

---

## Source → Facebook moves

| Source | Keep | Change | Strip |
|---|---|---|---|
| LinkedIn post | The insight, the number | Corporate tone → plain and warm | Buzzwords, "Agree?", hashtag block |
| X thread | The arc | Stitch into one readable story | "1/", "🧵", @handles |
| Blog / newsletter | One relatable angle | Lead with the human moment | "In this post", subheads, summary tone |
| YouTube script | The payoff | Put the payoff first | "In this video", subscribe asks |
| Instagram / TikTok caption | The one line that carries | Fewer emoji | Hashtag walls, "link in bio" |

---

## Rules

1. **Claims and numbers never change.** Delivery changes. Meaning doesn't.
2. **Never paste and trim.** Rebuild from the spine.
   - Bad → the LinkedIn post with "Agree?" deleted.
   - Good → a new post built on the same fact.
3. **Line one carries the whole point.**
4. **Warm, not clickbait.** No "You won't BELIEVE". No ALL CAPS.
5. **No engagement bait.** No "tag 3 friends", no "share if you agree".
6. **Never admit it's repurposed.** No "As I posted on LinkedIn...".
7. **0 to 2 hashtags, 0 to 2 emoji.**
8. **Never invent the human detail.** Ask for it.

---

## Worked example

**Source (X thread, 6 tweets):** "1/ I tracked every hour I spent on my newsletter for 90 days. 🧵 2/ Writing took 31%. 3/ Editing 18%. 4/ Finding images 22%. 5/ Formatting 29%. 6/ I now batch images and use a template. Saves 4 hrs/week."

**Spine:** Half my newsletter time wasn't writing.

**Option 1 — F2 Small Number (short, shares)**
```
Half the time I spend on my newsletter isn't writing. It's images and formatting.
```

**Option 2 — F8 Story With a Turn (long, comments)**
```
I timed every hour on my newsletter for 90 days.

I expected writing to eat most of it. It was 31%.

Images took 22%. Formatting took 29%. Half my week was going on things readers barely notice.

Now I batch the images on Mondays and use one template. I got 4 hours a week back.

What's the part of your work that takes longer than it should?
```

Mapping: tweets 2–5 → the numbers paragraph. Tweet 6 → the turn. Thread numbering and 🧵 stripped.

---

## Output format

```
## Facebook version of: [source, one line]
Spine: [one sentence]
Destination: [ ]   Goal: [ ]

### Option 1 — [shape]
[post]
Characters: [n]

### Option 2 — [shape]
[post]

Mapping: [what became what]
Link handling: [in post / first comment / none]
Group rules check: [done / not applicable / need rules pasted]
```

---

## Sibling skills

- `fb-postiz-publisher` — schedule the finished post through Postiz after you approve it.
- `fb-post-writer`: start from scratch instead.
- `fb-humanizer`: final scrub.
- `fb-hook-extractor`: study the Facebook shape before rebuilding.
- `fb-content-planner`: slot repurposed posts into the week.
- `yt-repurposer`: when the source is a YouTube video and you need several formats.

---

## Pre-flight checklist

- [ ] Spine written in one sentence.
- [ ] Facts and numbers unchanged.
- [ ] Line one stands alone.
- [ ] Tone warmed. Source clutter stripped.
- [ ] Link trade-off explained.
- [ ] Group rules checked if posting in a Group.
- [ ] No invented details.
