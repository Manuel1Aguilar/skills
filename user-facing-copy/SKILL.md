---
name: user-facing-copy
description: Write or review any text a user will read — button labels, error messages, empty states, onboarding, notifications, marketing pages, privacy policies, App Store text, social captions, hooks and on-screen video text — so it reads as written by someone who knows the product rather than generated. Use before shipping any new user-facing string, and when reviewing existing copy.
---

# Writing copy that doesn't read as machine-written

The tells below are **cumulative, not binary**. One em dash proves nothing. A
paragraph with three of them, in prose that is fluent and says nothing checkable,
proves a great deal. Expert annotators identifying AI text cite vocabulary in
about half of judgments, sentence structure in a third, and "originality" and
"clarity" — meaning *it says nothing specific* — in about a fifth each.

**The most important consequence:** blandness is the tell that survives rewriting.
Swapping banned words for permitted ones changes nothing if the sentence still
makes no checkable claim. Fix the emptiness first, the vocabulary second. (By
blandness we mean *no checkable fact*, not a flat tone. Flat tone on its own is a
weak signal.)

The tells also drift as models change. Word lists and em dashes date fastest;
structure lasts. A 2026 study separated AI blog posts from human ones at ~97 F1
on structural features alone, and still ~96 after paraphrasing. So check the
shape of the text before you grep for words.

## Do not churn good copy

The failure mode of this skill is rewriting text that was already fine, to make
it differ from a word list. Short, plain, specific copy should be left alone, and
you should say which strings you left and why. On one real pass over an iOS app,
two of six copy files came through **completely unchanged** and that was the
correct outcome.

## The four things to fix, in order

### 1. Fluent and factless
The strongest long-form tell. Every screen of prose should contain at least one
concrete, checkable thing: a number, a location, a retention period, a real
limitation.

- ✗ "We are committed to safeguarding your data with industry-leading security."
- ✗ "Your meals are yours, and deleting your account really deletes them."
- ✓ "Your photos sit on a server we rent in Germany. Delete account takes them off
  it straight away."

Two tests:
- **Swap test.** Replace your product's name with a competitor's. If the sentence
  still works, it says nothing about your product. Rewrite it around something
  only yours does.
- **Specific-detail test.** Can the reader check any claim in this paragraph? If
  not, it is decoration.

### 2. Structural tells
- **Negative parallelism** — "not just X, it's Y", "not only… but also", "rather
  than". Humans write these occasionally; models write one per paragraph. Its
  split form is the strongest tell in short copy: "It's not a timer. It's a
  coach." / "The ghost wasn't scary. The next step was." Also "No gym. No coach.
  Just your phone." (negation triplet). Say the thing directly: "Step 2 is where
  people quit: the form asks for your tax ID."
- **Self-answered questions and false suspense** — "The secret? Consistency.",
  "Here's the kicker:", "Here's where it gets interesting:". State the fact.
- **Staccato fragments** — three short fragments in a row for drama: "Traffic
  dropped. Rankings vanished. The client called." Join them into a sentence that
  carries the cause: "Traffic dropped 40% overnight, and by lunch the client had
  called."
- **Quotable closers** — a wise-sounding last line that adds no information:
  "Because the best workout is the one you finish." End on the last fact, the
  question, or the call to action.
- **Rule of three** — triplets of adjectives or benefits, used to make thin
  content look complete. Use two, or four, or rewrite flat. (A list of three
  *real* things is fine: "the plate, the label and the packet" is a fact.)
- **Sentence-final "-ing" clauses** asserting benefit: "…, ensuring accuracy",
  "…, helping you stay on track", "…, making it easier than ever". Delete them.
  The sentence is almost always complete without, and loses no information.
- **Bold-header-colon bullets** — `**Thing:** description` repeated down a list.
  A named structural tell. Write sentences.
- **Uniform rhythm** — every bullet the same length and shape, every paragraph
  three sentences, every section ending in a restatement. Vary something. Newer
  models that dropped em dashes produce the same thing with full stops instead:
  sentence after sentence of 8–20 words. Look at a run of sentence lengths, not
  only the punctuation.
- **Self-announcing structure** (long form) — thesis before any content ("X is
  broken."), a preview of the sections, the subject set against "the old way",
  and a closing summary. Start with the first useful fact.
- **Restating the control** — prose above a button that describes the button.
  If a note says "…and can be uploaded again" above an *Upload again* pill, cut it.
- **Over-signposting** — "Here's the thing:", "In this section we'll explain",
  rhetorical questions used as transitions. (Genuine FAQ headings are fine.)

### 3. Vocabulary
Replace, don't just delete. The GOV.UK substitutions are the most useful because
they give the replacement: *empower* → let / allow; *leverage* / *utilise* → use;
*robust* → well thought out; *streamline* → simplify; *facilitate* → say what you
actually do; *foster* → encourage; *deliver* (abstractions) → make, provide;
*impact* → affect; *initiate* → start; *going forward* → from now on; *in order
to* → delete; *key* (adjective) → important, or delete.

Also avoid: seamless, effortless, elevate, unlock, journey, insights,
comprehensive, delve, crucial, pivotal, underscore, showcase, enhance,
emphasizing, highlighting, multifaceted, cutting-edge, best-in-class,
industry-leading, committed to, simply, just, ensure. These lists date: each
model generation has its own favourites, so expect them to keep changing.

**Magic adverbs** that add mood but no fact: *quietly*, *deeply*,
*fundamentally*, *remarkably*. "The app quietly tracks your rest" → "The app
times your rest."

Connectives such as *Additionally*, *Moreover*, *Furthermore*, *That said*,
*It's worth noting*, *In summary*, *Ultimately*, *At its core* and *When it comes
to* are weak on their own. Count them only when they appear alongside other tells.
Vague links ("associated with", "connected to") where a person would name the
relation are a stronger current sign.

Chat residue that leaks into shipped strings: *Certainly!*, *Of course!*, *Great
question*, *Here's a breakdown*, *Let me know if…*, *I hope this helps*.

**Copula avoidance** (*serves as*, *stands as*, *functions as*, *boasts* where a
person writes *is* or *has*) is mostly a tell of older models now, but it is
still worth fixing because *is* reads better.

### 4. Punctuation and tone
- **Spaced em dashes** ( — ) used as a rhythm crutch where a comma, colon or full
  stop belongs. Keep the ones doing real parenthetical work; cut the rest. A
  budget of one or two per screen is generous. Most newer models have stopped
  overusing them, so text without dashes is not proof of anything. Some models
  still overuse them, so keep the budget.
- **Exclamation points** — near zero. **Emoji** — only where they carry meaning,
  never as bullets or section markers.
- **One quote style, one apostrophe style, one capitalisation rule per element
  type**, enforced in the strings file. Mixed straight and curly quotes in one
  file is itself the tell.
- **No unearned enthusiasm.** Congratulation belongs to something the user worked
  for, not to logging a sandwich.
- **No "Oops" or "Uh-oh".** Apple's own guidance calls these insincere.
- **Don't explain the obvious** or restate a label in its own description.
- Use possessives sparingly ("Favourites", not "Your Favourites"). Avoid "we" —
  "Unable to load content" beats "We're having trouble loading this content".

## UI microcopy specifics

**Buttons** name the outcome with a verb, in sentence case. "Log meal", not
"Submit". "Save", not "Confirm Selection". Never name the mechanism: "analysis
engine", "sync status", "entitlement" are internal words.

**Errors** say what happened, what the user can do, and preserve their input.
Never *invalid*, *illegal*, *incorrect*, *failed* at the user. Never "Something
went wrong. Please try again later." with nothing after it.
- ✗ "Invalid input" → ✓ "Enter weight in kg, like 74.5"
- ✗ "Failed to analyse image" → ✓ "Couldn't read that photo. Try better light, or
  type what you ate."
If the user cannot fix it, it should not be a field-level error at all.

**Empty states** guide to the next action and give a control to do it. Not
congratulation ("You're all set! 🎉"), not poetry ("Your journey starts now").

**Feature descriptions** name the result, not the mechanism. "Powered by advanced
AI vision models" → "Take a photo, get the calories."

## Social copy: captions, hooks, on-screen text

Short copy has few words to hide in, so one tell is enough to give it away. The
ones that show up most:
- The split contrast reveal ("X wasn't A. B was.") as the hook or the last line.
- Staccato fragment triplets ("I froze. Didn't answer. Ever.").
- An aphorism or moral as the closer.
- Objects given dramatic one-liners ("The kettle knew."). We learned this one
  from feedback; we haven't seen it in a published source.
- Manufactured vulnerability ("I'll be honest:", "Real talk:").
- Every setback turned into a lesson ("Losing the streak taught me something").

Write it the way the audience would caption it themselves: plain, concrete, the
payoff action early. "I lost the streak on day 12. Flu." These patterns are
regular enough to lint for. Run a regex check before anything ships and treat
each hit as a forced rewrite. An LLM reviewer asked to spot them misses some.

**Spanish:** the evidence is thinner. Exploratory work reports full stops as
nearly the only punctuation, rigid word order, and English calques: too many
gerunds and paired adjectives. The same contrast patterns ("no es X, es Y",
"X no daba miedo. Y sí.") are the strongest tells in Spanish too.

**Privacy and legal text**: GDPR Art. 12 *requires* "clear and plain language", so
simplifying is compliance, not risk. Answer the questions people actually search:
what happens to my photos, where are they, who sees them, how do I delete
everything. State facts, not assurances.

## Constraints that outrank style

Before rewriting, find out which strings are load-bearing, and treat them as
fixed:
- **Legal and review wording.** Account deletion copy that lists what is erased,
  states permanence, and separates deletion from subscription cancellation is
  checked by App Review. A purchase failure must say nothing was charged.
- **Facts in a published policy.** Style may change; claims may not. Re-verify
  each against the source before and after.
- **Strings asserted by tests**, matched by UI tests, or fixed by a design
  handoff. Changing one means updating the test in the same edit.
- **Platform-mandated labels** ("Sign in with Apple").

When copy comes from a designer, check the design source before inventing a
replacement — the better line is often already there.

## Reviewing at scale

Split by file area and run reviewers in parallel over **disjoint** file sets so
they cannot collide. Require each to report: what changed with before → after and
a one-line reason, what was deliberately left alone, and which tests it updated.
An agent that reports no exceptions has probably churned good copy.

Watch for cross-area coupling: a string in a shared module may be asserted by a
test in an area another reviewer owns.

## Checklist

1. Grep for the vocabulary lists. Replace with the substitution, not a deletion.
2. Search "not just", "not only", "rather than", and the split form "isn't X.
   Y is." — flatten.
3. Count triplets. Cut to two or four unless the three things are real.
4. Delete sentence-final "-ing" benefit clauses. Check nothing was lost.
5. Count spaced em dashes. Keep the parenthetical ones only.
6. Read each string aloud in a shop-queue voice. Would you say it to a friend?
7. Swap test — does it survive renaming to a competitor?
8. Mechanism test — outcome or internals?
9. Error triage — what happened, what next, input preserved?
10. Emotion audit — exclamation points, emoji, congratulation. Budget near zero.
11. Rhythm audit — is every bullet the same length and shape?
12. Specific-detail test — one checkable fact per screen of prose.
13. Last line — is it a fact or a question, not a moral? First line — is it
    the payoff, not a self-answered question?

## Sources

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [Russell, Karpinska & Iyyer, ACL 2025 — expert human detectors](https://aclanthology.org/2025.acl-long.267/)
- [Reinhart et al., PNAS 2025 — Do LLMs write like humans?](https://pnas.org/doi/10.1073/pnas.2422455122)
- [SlopShape, arXiv 2609.15369 — structural features of AI blog prose](https://arxiv.org/abs/2609.15369)
- [tropes.fyi — catalogue of AI writing tropes](https://tropes.fyi/) (practitioner, no data)
- [Momentic — avoiding AI slop](https://momenticmarketing.com/blog/avoid-ai-slop) (practitioner)
- [TechCrunch 2026 — "it's not just this, it's that" in corporate releases](https://techcrunch.com/2026/04/20/ai-writing-its-not-just-this-its-that-barrons/)
- [Apple HIG — Writing](https://developer.apple.com/design/human-interface-guidelines/writing)
- [GOV.UK A–Z style guide (words to avoid)](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style)
- [NN/g — Error-Message Guidelines](https://www.nngroup.com/articles/error-message-guidelines/)
- [Mailchimp Content Style Guide](https://styleguide.mailchimp.com/)
- [GDPR Art. 12 — clear and plain language](https://gdpr-info.eu/art-12-gdpr/)
