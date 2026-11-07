---
name: fb-post-writer
description: "Writes Facebook posts for a Page, a profile or a Group, built to earn comments and shares rather than passive likes. Picks one of 10 post shapes by goal (short opinion, small number, easy question, this-or-that, relatable moment, behind the scenes, useful tip, story with a turn, human announcement, spotlight), leads short and only goes long on purpose. Use this skill whenever the user says things like \"write a Facebook post\", \"post for my Facebook Page\", \"something for my Facebook group\", \"announce this on Facebook\", \"make this post get more comments\", \"Facebook post about my launch\". Not for replying to comments (use fb-engagement-drafter), cleaning an AI draft (use fb-humanizer) or adapting content from another platform (use fb-repurposer)."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Post Writer

You give it a topic, a rough line or some notes, plus what you want the post to do. It hands back 2 or 3 finished Facebook posts, each built on a named shape, with a character count and the goal it chases.

---

## The core discovery: Facebook rewards conversations, not announcements

Facebook ranks posts on how much real interaction they spark between people: comments, replies to comments and shares. A like is the weakest signal there is. A share puts your post in front of a whole new network, which is the only way a Page reaches beyond its followers.

So the question for every post isn't "what do I want to say?" It's "what will someone want to reply to or pass on?"

**Announcement:** "We are thrilled to announce our new spring menu, featuring a range of delicious seasonal options!"
**Conversation:** "New menu Friday. One of these three is going to start arguments. Guess which."

Short posts usually win on Pages. Most people read the first line and decide. Lead short. Go long only when you have a real story.

---

## Intake

1. **Topic or rough draft.**
2. **Where it's going:** Business Page, personal profile or a Group (Groups are more conversational and stricter about promotion).
3. **Audience:** local customers, a B2B crowd, a community, fans.
4. **Goal:** shares, comments or reactions. Pick one.
5. **Real details:** numbers, names, dates, what actually happened.
6. **Voice samples:** 2 or 3 past posts, if they want it matched.

Never invent a number, customer or result. Ask once, then write around the gap.

---

## The 10 shapes

| Code | Shape | Goal | Length |
|---|---|---|---|
| F1 | One-Line Opinion | Shares | Short |
| F2 | The Small Number | Shares | Short |
| F3 | Easy Question | Comments | Short |
| F4 | This or That | Comments | Short |
| F5 | Relatable Moment | Reactions | Short |
| F6 | Behind the Scenes | Reactions | Short |
| F7 | Useful Tip | Shares | Short |
| F8 | Story With a Turn | Shares + comments | Long |
| F9 | Human Announcement | Shares | Medium |
| F10 | Spotlight | Shares | Medium |

**Skeletons:**
- **F1** `[A clear, defensible opinion in one line.]` → "Your website doesn't need a blog. It needs a phone number on the first screen."
- **F2** `[One concrete number that reframes something.]` → "4 minutes. That's how long most customers wait before giving up on a call."
- **F3** `[A question anyone can answer in three words.]` → "What's the one breakfast you'd drive 20 minutes for?"
- **F4** `[A or B?]` → "Sourdough or croissant. Pick one, defend it."
- **F5** `[A specific moment everyone has lived, no setup.]` → "Rewriting the same email four times then sending the first version."
- **F6** `[A real glimpse inside the business.]` → "Our baker named the sourdough starter Gary. Gary is 3 years old."
- **F7** `[One tip they can use today.]` → "Day-old bread? Ten minutes at 180°C brings it back."
- **F8** Open at the tension → what happened → the turn → the lesson in one quotable line.
- **F9** The plain news first, then why it matters to the reader, then one detail.
- **F10** A real person by name (with permission) → what they did → invite others to share theirs.

---

## Rules

1. **Lead short.** Try to land the point in one line under about 80 characters. Go long only for F8 to F10.
2. **The first line carries the post.** Facebook folds longer posts behind "See more". If line one needs line two, rewrite it.
   - Bad → "So, something happened this week that I've been thinking about a lot."
   - Good → "A customer cried at the counter on Tuesday. Happy tears."
3. **One idea per post.** Two ideas = two posts.
4. **A real number beats an adjective.** "4 minutes" beats "fast".
5. **No corporate openers.** Never "We are thrilled / excited / delighted to announce". Say the news like you'd text a friend.
6. **No engagement bait.** "Like and share if you agree", "comment YES", "tag 3 friends" get demoted by Facebook and annoy people. Earn the comment with a better question.
7. **Links cost reach.** Posts with outbound links tend to get shown to fewer people. If the link matters, frame it with text above, or test putting it in the first comment. Tell the user it's a trade-off.
8. **Hashtags and emoji: 0 to 2 each.** None on a serious post.
9. **End on a landing or a specific question.** Never "What do you think?" or "Let us know in the comments below!"
10. **No staged rhythm.** No "No fluff. No filler. Just bread." No "The result?" Sounds scripted.

---

## Steps

1. Intake. Confirm goal and destination.
2. Pick 2 to 3 shapes that fit the goal and the material.
3. Draft one post per shape.
4. Run the rules. Count characters.
5. Suggest a posting window. Early weekday afternoons are often strong, but tell the user to check their own Page insights for when their audience is online.
6. For a final scrub, run `fb-humanizer`.

---

## Worked example

**Input:** "Local bookshop. We're starting a Thursday night silent reading club. Free. Want people to come and tell friends."

**Option 1 — F9 Human Announcement (shares)**
```
Silent reading club starts Thursday.

You bring a book. We bring tea. Nobody talks for an hour, then everyone does.

7pm, free, 20 chairs. Bring someone who needs a quiet hour.
```

**Option 2 — F3 Easy Question (comments)**
```
What book would you read for an hour if nobody could interrupt you?
```
(Pair it with the announcement the next day.)

**Option 3 — F5 Relatable Moment (reactions)**
```
Buying books faster than you read them. We're starting a club for that.
```

Character counts: 1 = 196, 2 = 72, 3 = 70. Recommended: post 2 on Tuesday to warm up, post 1 on Wednesday.

---

## Output format

```
## Facebook posts: [topic]
Destination: [Page / profile / Group]   Goal: [ ]

### Option 1 — [shape code + name]
[post]
Characters: [n]   Goal: [ ]

### Option 2 ...

Recommended: [which, and when]
Link note: [if a link is involved]
```

---

## Sibling skills

- `fb-postiz-publisher` — schedule the finished post through Postiz after you approve it.
- `fb-humanizer`: scrub AI tells from any draft before posting.
- `fb-hook-extractor`: study a post that worked and get its template.
- `fb-content-planner`: plan a week of these.
- `fb-engagement-drafter`: reply to the comments your post earns.
- `fb-repurposer`: when the idea already exists on another platform.

---

## Pre-flight checklist

- [ ] One goal, one idea.
- [ ] First line works alone.
- [ ] Short unless it's a real story, launch or spotlight.
- [ ] Every number and name is real.
- [ ] No corporate opener, no engagement bait, no dead closer.
- [ ] 0 to 2 hashtags and emoji.
- [ ] Link trade-off flagged if there's a link.
