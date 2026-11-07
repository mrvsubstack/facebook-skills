---
name: fb-content-planner
description: "Builds a weekly Facebook plan for a Page, a Group or both: content pillars with weights, a day-by-day grid (post shape, angle, goal, time), a short-to-story mix, Group prompts and a daily reply routine, then runs a balance check so the week isn't all promotion or all questions. Use this skill whenever the user says things like \"plan my Facebook week\", \"what should my Page post this week\", \"Facebook content calendar\", \"posting schedule for my Facebook group\", \"I post randomly on Facebook\", \"plan Facebook posts for my launch\". Not for writing one post (use fb-post-writer) or replying to comments (use fb-engagement-drafter)."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Content Planner

You give it your audience, what you're promoting (if anything) and how often you can post. It hands back a 7-day plan where every slot already has a post shape, an angle, a goal and a time, plus a reply routine and a balance check.

It plans. `fb-post-writer` writes each post.

---

## The core discovery: promotion borrows reach that value posts earned

A Page that only sells gets shown to fewer and fewer people. Every post that nobody comments on teaches Facebook your Page is boring. Then the launch post arrives and nobody sees it.

The fix is a ratio. Most posts give (useful, funny, human, conversational). A few ask. The giving posts build the reach the asking posts spend.

**Drifting week:** 5 promo posts, 2 reposts, 0 comments.
**Planned week:** 3 value, 2 community, 1 behind-the-scenes, 1 promo. The promo lands on a warm audience.

---

## Intake

1. **Page, Group or both.**
2. **Audience** in one line ("local families who brunch on weekends", "freelance designers").
3. **This week's theme or launch**, if any.
4. **Capacity:** posts per week you can actually produce. Default 5 to 7.
5. **Pillar preferences**, or accept the defaults below.
6. **Timezone** and any insights data on when followers are online.
7. **Past posts that worked**, to repeat their shapes.

---

## Default pillars

| Pillar | Weight | Does | Shapes (from fb-post-writer) |
|---|---|---|---|
| Value | 40% | Teaches or helps. Gets shared. | F1 Opinion, F2 Small Number, F7 Useful Tip |
| Community | 30% | Starts conversations. Gets comments. | F3 Easy Question, F4 This or That, F10 Spotlight |
| Behind the Scenes | 20% | Shows the humans. Builds trust. | F5 Relatable, F6 Behind the Scenes, F8 Story |
| Promotion | 10% | Sells or launches. | F9 Announcement, F10 Spotlight with a result |

**Adjusting:**
- New Page → Community up to 50% to seed comments.
- Loyal audience → Value up to 50%.
- Launch week → Promotion up to 20%, every promo post still human.
- Local business → Behind the Scenes up to 30%.

---

## Rules

1. **No pillar over 60% of the week.** All value reads like a blog. All community reads needy.
2. **Promotion stays smallest.** One or two posts a week.
3. **Lead short.** About 70% short posts, 30% longer stories. Short posts carry engagement. Stories are deliberate.
4. **At least 2 share-goal posts.** Shares are how a Page reaches past its followers.
5. **At least 1 comment-goal post and 1 human post.**
6. **No shape more than twice a week.** Repetition reads engineered.
7. **Replies are part of the plan.** Block 15 minutes after each post. Replying in the first hour keeps the post alive. Questions and complaints first.
8. **Groups get prompts, not ads.** In a Group, schedule recurring threads (weekly wins, Monday questions, feedback Fridays) and keep promotion to what the Group rules allow.
9. **Times are a starting point.** Early weekday afternoons are commonly cited as strong. Check Page insights and say which you used.

---

## Steps

1. Intake. Fill gaps with defaults and say so.
2. Validate the pillar weights total 100%. Warn if any is over 60%.
3. Fill each day: short or story, pillar, shape, one-line angle, goal, time.
4. Add a Group prompt slot if there's a Group.
5. Add the daily reply routine.
6. Run the balance check. Fix and re-run until it passes.
7. Hand each slot to `fb-post-writer`.

---

## Worked example

**Input:** Neighbourhood bakery Page + a small "regulars" Group. Theme: spring menu launches Monday. 7 posts. UK, followers online lunchtime.

| Day | Type | Pillar | Shape | Angle | Goal | Time |
|---|---|---|---|---|---|---|
| Mon | Short | Value | F7 Tip | "Day-old bread, 10 minutes at 180°C" | Shares | 12:30 |
| Tue | Short | Community | F4 This or That | "Sweet or savoury Saturday?" | Comments | 12:30 |
| Wed | Story | Behind the Scenes | F8 Story | "The 4am oven that died before our busiest day" | Shares | 13:00 |
| Thu | Short | Value | F2 Small Number | "We bake 212 loaves before 9am" | Shares | 12:30 |
| Fri | Short | Community | F3 Question | "Which pastry should we bring back?" | Comments | 12:00 |
| Sat | Story | Community | F10 Spotlight | "Margaret, here every Saturday since 2019" (with permission) | Shares | 10:00 |
| Sun | Short | Promotion | F9 Announcement | "Spring menu Monday. Three new things." | Shares | 11:00 |

**Group:** Wednesday "What are you baking this weekend?" thread. Friday: share the winner of the pastry vote.

**Reply routine:** 15 minutes after each post. Answer questions, thank with a detail, move complaints to DM.

**Balance check:** Value 29% / Community 43% / BTS 14% / Promo 14% ✓ no pillar over 60%. Short 5, story 2 ✓. Share-goal 5 ✓. Comment-goal 2 ✓. No shape repeated over twice ✓.

---

## Output format

```
## Facebook plan: [Page/Group] — week of [date]
Pillar weights: [ ]
Timezone: [ ]   Times based on: [insights / general guidance]

| Day | Type | Pillar | Shape | Angle | Goal | Time |

Group prompts: [ ]
Reply routine: [ ]

Balance check:
- Pillars: [ ] (none over 60%)
- Short/story: [ ]
- Share-goal posts: [n] (≥2)
- Comment-goal posts: [n] (≥1)
- Human post: [y/n]
- Repeated shapes: [ ]
```

---

## Sibling skills

- `fb-post-writer`: write each slot.
- `fb-engagement-drafter`: run the reply routine.
- `fb-hook-extractor`: study competitors' winning posts while planning.
- `fb-repurposer`: fill slots with content you already made elsewhere.
- `fb-humanizer`: scrub each draft before it ships.

---

## Pre-flight checklist

- [ ] Every slot has type, pillar, shape, angle, goal and time.
- [ ] Balance check passes.
- [ ] Promotion is the smallest pillar.
- [ ] Reply routine included.
- [ ] Group slots are prompts, not ads.
- [ ] Times labelled as insights-based or general guidance.
