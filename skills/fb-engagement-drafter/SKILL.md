---
name: fb-engagement-drafter
description: "Drafts replies to comments on your Facebook posts, and helpful comments on other people's posts and Groups, in your voice. Sorts comments by type (question, praise, complaint, win, troll), picks one of 6 reply moves for each and writes 1 to 3 short variants you paste in yourself. Use this skill whenever the user says things like \"reply to these Facebook comments\", \"how do I answer this complaint\", \"someone left a bad comment\", \"help me respond to my Page comments\", \"write a comment for this group post\", \"keep the conversation going on my post\". Not for writing new posts (use fb-post-writer)."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Engagement Drafter

You paste the post and the comments under it. It hands back a reply for each comment worth answering, labelled with the move it uses, ready to paste into Facebook or Meta Business Suite.

You post the replies yourself. That's the point: real replies from a real person.

---

## The core discovery: every reply is a second post

When you reply to a comment, the commenter gets notified, often comes back, and sometimes replies again. That back-and-forth is exactly what Facebook reads as a post worth showing to more people. A Page that answers fast gets more reach on that post.

But only if the reply gives them something to answer.

**Dead end:** "Thanks so much! 😊"
**Second post:** "Thank you. The Saturday batch is the one to beat. Ask for it warm and tell me if I'm wrong."

The first closes the thread. The second reopens it.

---

## Intake

1. **The post** (for context).
2. **The comments**, pasted in. Claude can't read Facebook directly.
3. **Your voice:** 2 or 3 past replies or posts, or a few words ("warm, dry humour, never corporate").
4. **Anything off-limits:** refund policy, topics you don't discuss publicly, what moves to DM.
5. **Your facts:** opening hours, prices, links, so answers are accurate. Never guess a fact.

---

## Step 1: Sort the comments

| Type | Example | Priority |
|---|---|---|
| Question | "Are you open Sunday?" | 1 |
| Complaint | "Waited 30 minutes, not impressed" | 1 |
| Win / story | "Made your recipe, kids loved it" | 2 |
| Praise | "Best sourdough in town!" | 2 |
| Opinion / debate | "Croissants are overrated" | 3 |
| Troll / spam | Abuse, scams, bait | Hide or ignore |

Questions and complaints first. They're the ones other people are watching.

---

## Step 2: Pick a move

| Code | Move | Use for | Shape |
|---|---|---|---|
| R1 | Straight Answer | Questions | The answer + one useful detail |
| R2 | Thanks Plus | Praise | Thank them + add something new |
| R3 | Own It | Complaints | Acknowledge → own it → next step → DM if details needed |
| R4 | Keep It Going | Positive comments, debates | Build on what they said + an easy follow-up |
| R5 | Spotlight Invite | Wins and stories | Celebrate + ask if you can share it (feeds a future spotlight post) |
| R6 | Calm Exit | Hostile but real people | One polite, factual line. No argument. |

---

## Rules

1. **Reply fast, keep it human.** A quick real reply beats a slow polished one.
2. **Never a canned thank-you.** "Thank you for your feedback!" says nobody read it. Add a detail or don't reply.
   - Bad → "Thanks for your comment!"
   - Good → "Thank you. That loaf took us 2 years to get right."
3. **Answer the actual question first.** Then add one detail.
   - Bad → "Great question! We'd love to see you!"
   - Good → "We are. 8 to 2 on Sundays. Come early for the cinnamon rolls."
4. **Complaints: acknowledge, own, offer, move.** Never argue in public. Everyone sees it, and screenshots last forever.
   - Bad → "We were very busy that day, as anyone could see."
   - Good → "30 minutes is too long, and I'm sorry. We were a baker down Saturday. Can you message us? I'd like to make the next one on us."
5. **Don't promise what you can't deliver.** No refunds, freebies or fixes the user hasn't approved.
6. **Don't sell in replies.** Mention the product only if it truly answers the question.
7. **Keep it to a few short lines.**
8. **Don't feed trolls.** Hide abusive comments, delete spam, report scams. Don't write a reply. Tell the user which to hide.
9. **Ask before quoting or featuring anyone.**
10. **Commenting on other people's posts or in Groups:** add a real experience or useful answer. Never drop a link to your stuff unless asked. In Groups, follow the Group's rules on self-promotion.

---

## Modes

### Mode 1: Reply queue
**When:** the user pastes comments from their own post.
**How:** sort, pick moves, draft 1 to 3 variants per comment, flag any to hide.

### Mode 2: Crisis comment
**When:** one angry comment is drawing attention.
**How:** draft an R3 or R6 reply, plus a short DM to send privately. Tell the user to check facts before replying, and not to delete a legitimate complaint (it usually makes things worse).

### Mode 3: Outbound comments
**When:** the user wants to comment on other Pages or in Groups to build presence.
**How:** ask for the post text. Draft a comment that adds an experience, a specific tip or a thoughtful question. No pitch.

---

## Worked example

**Post:** "New spring menu starts Monday."
**Comments pasted:**
1. "Is the lemon tart staying?"
2. "Came Saturday, waited 25 min for a coffee."
3. "Your cardamom buns got me through exams last year 😂"

**Replies:**
1. **R1 Straight Answer:** "It's staying. It outvoted everything else in March."
2. **R3 Own It:** "25 minutes for a coffee isn't okay, and I'm sorry. Saturday we were two people short. Message us and the next one's on us." *(Check: is a free coffee approved?)*
3. **R5 Spotlight Invite:** "This made our morning. Exams AND cardamom buns. Could we share this on the Page? Happy to tag you or keep it anonymous."

---

## Output format

```
## Replies for: [post, one line]

### Comment 1: "[quoted comment]"
Type: [ ]   Move: [R1–R6]
Variant A: [reply]
Variant B: [reply, optional]

...

Hide / ignore: [comment numbers + reason]
Needs your OK: [any promise, refund or quote]
```

---

## Sibling skills

- `fb-post-writer`: write the next post, maybe from a great comment.
- `fb-content-planner`: schedules the daily reply routine.
- `fb-humanizer`: scrub a reply that sounds corporate.

---

## Pre-flight checklist

- [ ] Questions and complaints answered first.
- [ ] No canned thank-yous.
- [ ] Every fact (hours, prices, policy) came from the user.
- [ ] Complaints acknowledged, owned and moved to DM. No arguments.
- [ ] No unapproved promises.
- [ ] Trolls flagged to hide, not answered.
- [ ] Permission asked before featuring anyone.
