---
name: fb-page-optimizer
description: "Audits a Facebook Page and rewrites what's failing: action button, intro and About, category, Page name, username and URL, featured or pinned post, cover photo, profile picture, and contact and link fields. Returns a 9-part scorecard, fixes ranked by impact and before → after rewrites matched to your goal (followers, leads, sales or community). Use this skill whenever the user says things like \"audit my Facebook Page\", \"fix my Page about section\", \"what button should my Page have\", \"rewrite my Facebook intro\", \"cover photo ideas\", \"my Page looks unfinished\", \"optimize my business Page\". Not for writing posts (use fb-post-writer) or planning a week (use fb-content-planner)."
metadata:
  author: Mr V
  version: "1.0"
  group: Facebook
---

# Facebook Page Optimizer

You give it your Page link or screenshots, plus what you want visitors to do. It hands back a 9-part scorecard, the fixes in order of impact and rewritten copy for every part that fails.

---

## The core discovery: the top of the Page does the selling

A visitor lands on your Page from a post, a search or a friend's share. They see the name, the profile picture, the cover, the intro line and the action button. They decide in about two seconds.

Most Pages waste that moment. The intro says when the business was founded. The button is missing or set to something irrelevant. The cover is a stock photo.

**Leaking:** "Rivera Bakery. Est. 2015. Family-owned and passionate about quality." Button: none.
**Converting:** "Rivera Bakery · Sourdough baked before 7am, every day. Pre-order for Saturday." Button: Order Food.

The button is the job of the Page. Everything else points at it.

---

## Intake

1. **Page link** plus screenshots of the top of the Page and the About section (Claude may not be able to load Facebook).
2. **Goal:** followers, leads, sales/bookings or community. One.
3. **Business type and location**, if local.
4. **Current button, category and username.**
5. **Best-performing posts**, to pick a featured post.
6. **The one link that matters.**

Facebook renames and moves Page features regularly. Verify current button options, character limits and cover dimensions in Facebook's help centre when web search is available, and label anything you couldn't confirm.

---

## The 9-part scorecard

Score each Pass / Needs work / Fail.

| # | Part | Passes when |
|---|---|---|
| 1 | Action button | Set, and matched to the goal (shop, book, sign up, message, call). |
| 2 | Intro / About | Leads with who it's for + what they get + one proof. Longer About carries hours, story, location. |
| 3 | Category | The most specific accurate one (Bakery, not Business). |
| 4 | Page name | Clear brand, plus a search word people type if it fits. Stable. |
| 5 | Username / URL | Custom, short, matches your other handles. |
| 6 | Featured post | Set. Your best proof or clearest offer. |
| 7 | Cover photo | One readable value line, safe from mobile cropping, reinforces the intro. |
| 8 | Profile picture | Logo or clear face, fills the circle, readable tiny. |
| 9 | Contact + links | Website, hours, address, phone, email as relevant. One goal-matched link. |

---

## Rules

1. **Match the button to the goal. One button, one job.**

| Goal | Button direction |
|---|---|
| Sales | Shop / Order |
| Appointments | Book |
| Leads / email list | Sign up |
| Enquiries / community | Send message / Call |

2. **Intro formula: who you serve + what you offer + one proof or specific.**
   - Bad → "Passionate about helping businesses grow since 2012."
   - Good → "Bookkeeping for Leeds cafés and restaurants. Monthly accounts in 5 working days."
3. **Benefit first, history later.** Founding dates and mission statements go in the longer About.
4. **Most specific category wins.** It shapes where you show up and unlocks the right fields (menu, services, booking).
5. **Name changes are slow.** Facebook reviews Page name changes. Get it right once.
6. **Claim the username.** A Page URL full of numbers looks unclaimed.
7. **The cover reinforces, never repeats.** One line, readable on a phone, away from the edges and the profile picture overlap.
8. **Blank fields read as closed.** Fill hours, address and contact for any local business.
9. **One primary link.** Several links? Use one link page, not five fields.

---

## Steps

1. Intake. Confirm the goal.
2. Score all 9 parts.
3. Rank fixes. Usual order: button → intro → featured post → cover → category → name/username → the rest.
4. Rewrite each failing part. Text gets before → after. Visuals get a short brief.
5. Pick the featured post with one line of reasoning.
6. Run the two-second test: read only the Page name, intro line and button. Would a stranger know who it's for and what to do? If not, rewrite.

---

## Worked example

**Input:** "Bright Minds Tutoring" Page. Goal: bookings. No button. Intro: "Welcome to Bright Minds! We love learning." Category: Education. Cover: stock image of books. URL: facebook.com/profile.php?id=1000…

**Scorecard excerpt:** Button Fail · Intro Fail · Category Needs work · Username Fail · Cover Fail.

**Rewrites:**
- Button → Book.
- Intro → "GCSE maths and English tutoring in Bristol. Small groups of 4, Saturday mornings."
- Category → Tutor/Teacher (or the closest specific option available).
- Username → facebook.com/brightmindsbristol.
- Cover brief → photo of a real session (with permission), text centred: "Small groups. Real progress. Saturdays." Keep text clear of the bottom left where the profile picture sits.
- Featured post → the parent testimonial post from March (most shares).

**Two-second test:** "Bright Minds Tutoring · GCSE maths and English tutoring in Bristol · [Book]" ✓

---

## Output format

```
## Page audit: [Page name]
Goal: [ ]

### Scorecard
| # | Part | Score | Note |

### Fixes by impact
1. ...

### Before → After
[part]: before / after

### Featured post pick
### Two-second test: [pass / fail + why]
Unverified: [any limits or features not confirmed]
```

---

## Sibling skills

- `fb-post-writer`: write the posts the Page will host, including a featured post.
- `fb-hook-extractor`: find a feature-worthy post that already worked.
- `fb-content-planner`: plan the posting rhythm.
- `fb-engagement-drafter`: handle the comments and messages the Page earns.

---

## Pre-flight checklist

- [ ] Goal named. Button matched to it.
- [ ] Intro leads with benefit + offer + proof.
- [ ] Most specific category chosen.
- [ ] Custom username recommended.
- [ ] Cover and profile picture briefs mobile-safe.
- [ ] Contact fields complete for a local business.
- [ ] Two-second test run.
- [ ] Facebook features and limits verified or labelled.
