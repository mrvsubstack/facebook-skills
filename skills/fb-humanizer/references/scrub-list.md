# Scrub list (Facebook Humanizer)

Load this when running Pass 1. Vocabulary is scored by density per paragraph. Patterns marked "always fix" are fixed on a single hit.

## Vocabulary markers (density-scored)

Each counts as one marker. Three or more in one paragraph means rewrite the paragraph.

| Marker | What to do when over the threshold |
|---|---|
| significant | Replace with the real number. Ask if there isn't one. |
| crucial, vital, essential | Delete, or say what happens if it's missing. |
| notably, particularly, especially | Delete. |
| comprehensive, holistic | "full", or name what's included. |
| insights | Say what was learned. |
| robust | "solid", or say why it holds up. |
| leverage, utilize, harness | "use". |
| foster | "build". |
| landscape, ecosystem, space | Name the actual market, town or group. |
| nuanced, multifaceted | Say the specific complication. |
| streamline | "simplify", or say what step was cut. |
| elevate, enhance | "improve", or say how. |
| empower | "let" or "help". |
| unlock | Say what they can now do. |
| navigate (figurative) | "handle", "get through". |
| seamless | "smooth", or describe the experience. |
| journey | Name the actual process. |
| game-changer | Say what changed. |
| deep dive | "a close look", or just the topic. |

Filler adverbs (one marker each): fundamentally, essentially, ultimately, truly, arguably, certainly, definitely, undoubtedly, simply.

## Grammar markers (density-scored)

- **"-ing" openers:** "Building on this, we..." → put the person first: "We built on this..."
- **"The [noun-ing] of":** "the implementation of the new menu" → "when we launched the new menu".
- **Stacked abstract nouns:** "alignment", "transformation", "optimization", "innovation", "synergy" near each other → say the concrete thing.

## Newer machine idioms (density-scored)

"quietly" (as in "quietly shipped"), "[X] matters." as its own line, "compounding", "a signal", "the work", "load-bearing", "doing the heavy lifting", "built different".

## Always fix (single hit)

**Corporate openers:** "We are thrilled / excited / delighted / proud to announce / share / introduce", "It is with great pleasure", "Big news!", "Exciting news!", "Without further ado".
→ Say the news plainly: "New menu Friday."

**Reveal bridges:** "The result?", "The best part?", "Here's the thing:", "Here's what nobody tells you", "Plot twist:", "Spoiler:", "Stop X. Start Y."
→ State the result directly.

**Contrast formulas:** "It's not X, it's Y.", "This isn't about X. It's about Y.", "Not just X, but Y."
→ Say Y.

**Announced honesty:** "Let me be honest", "I'll be real with you", "Honestly?", "Real talk", "Full transparency", "Not gonna lie", "Unpopular opinion:" (before a popular one).
→ Delete the frame. Keep the fact.

**Inserted hedges the user didn't write:** "perhaps", "it seems", "I might be wrong but".
→ Remove.

**Dead closers:** "What do you think?", "Let us know in the comments below!", "Thoughts?", "Let that sink in.", "That's the real story."
→ End on the landing or a specific question.

**Engagement bait:** "Like and share if you agree", "Comment YES", "Tag 3 friends who", "Type AMEN".
→ Remove. Replace with a real question if needed.

**Template leftovers:** [Your Name], [Business], [insert link], placeholder dates, cut-off citation markers, "As of my last update".
→ Flag. Ask the user to fill.

## Staged rhythm (always fix)

- "No X. No Y. Just Z."
- "All the X. None of the Y."
- Adjective stacks: "Simple. Fast. Effective."
- One-word paragraphs for drama: "Exactly." "Still."
- Q&A to self: "Why? Because..."
- Three or more standalone fragments in one post.

→ Merge into full sentences.

## Punctuation

- Curly quotes → straight quotes (if the user's other posts use straight).
- "--" → comma or rewrite.
- Em dashes: keep up to about one per 100 words. Replace extras with a comma, colon or parentheses. Never a full stop.

## Preserve (not tells)

- The user's ".." pauses, lowercase starts, regional spelling, slang.
- One natural list of three with concrete items.
- One em dash doing real work.
- Short paragraphs with blank lines between them.
