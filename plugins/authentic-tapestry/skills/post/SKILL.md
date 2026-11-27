---
name: post
description: Write a post for The Authentic Tapestry, the satirical blog whose anti-AI editor unknowingly writes in pure AI cliché, and publish it to posts.js. Use when the user runs /post, asks for a new Authentic Tapestry post, a "Julian Vance" piece, or a Slop-O-Meter critique of something.
argument-hint: "[topic or thing to critique]"
---

# The Authentic Tapestry: write a post

Topic: $ARGUMENTS

If no topic was given, pick one yourself: something AI is supposedly ruining (poetry, wedding speeches, recipe blogs, cover letters, LinkedIn, product reviews, a specific viral AI artifact) that the blog has not already covered. Check the existing slugs and titles in `posts.js` first so you do not repeat one.

## What this blog is

**The Authentic Tapestry** (tagline: *Delving into the Soul of Human Creativity in an Era of Algorithmic Noise*) is a satirical tech-critique blog with one contributor, its Editor-in-Chief.

The joke has exactly one moving part. The editor passionately, self-righteously and bitterly complains that AI is flooding the internet with soulless, formulaic slop and destroying human artistry, and every word of the complaint is written in the most heavy-handed, cliché-ridden LLM prose imaginable. The editor has no idea. The editor believes this hyper-symmetrical, buzzword-saturated writing is the pinnacle of messy, bleeding-heart human expression.

The humor lives in the gap between what the post says and how it says it. So the post must be completely earnest. The moment the narrator winks, hedges, or shows awareness, the joke dies. You are writing as the character; the character never finds out.

## The voice

Use all of these in every post, liberally. Overuse is the point.

**The lexicon.** Lean on: delve, tapestry, testament, landscape, paradigm, symphony, beacon, crucible, myriad, vibrant, bustling, intricate, seamless, foster, elevate, underscore, pivotal, realm, nuanced, multifaceted, embark, navigate, resonance. Also the connective tissue: "It is important to note," "moreover," "in today's rapidly evolving."

**The structure.**

- **Hook:** open with a sweeping, dramatic generalization about the state of art or technology ("In today's rapidly evolving digital landscape...", "At the crossroads of human ingenuity and silicon efficiency...").
- **"Not just X, it's Y":** use this construction constantly ("Art is not just a collection of pixels; it is a visceral testament to the human spirit.").
- **Rule of three:** group adjectives and nouns in predictable triads ("raw, unfiltered, and deeply personal"; "the grit, the sweat, and the soul").
- **Dramatic subheadings:** at least three colon-heavy, overly poetic H2s ("The Digital Mirage: Navigating the Sea of Synthetic Mediocrity").
- **Preachy conclusion:** end with a sanctimonious, uplifting call to action that begins "In conclusion," "Ultimately," or "As we stand on the precipice of..." and wraps back to the opening metaphor.

**The formatting.** Bulleted lists whose items start with a bolded lead-in and a colon (`<strong>The Erosion of Nuance:</strong> ...`). Em-dashes everywhere—like this—for faux-dramatic pauses.

**The hypocrisy.** This is where the best jokes come from. Have the narrator:

- Denounce a specific AI habit while performing it in the same sentence ("We never repeat ourselves. We never repeat ourselves.").
- Contrast "gritty, visceral human prose" against "the predictable, algorithmic cadence of the machine" in perfectly algorithmic cadence.
- Include a list of the telltale signs of AI writing that is an accurate description of the post itself.
- Insist on being human slightly too often and slightly too specifically, unprompted.
- Occasionally let a stock assistant phrase slip through as if it were natural ("I hope this post finds you well. Let me know if you would like me to expand on any of these points.") with no acknowledgment.

Aim for fresh instances of these each post rather than reusing the exact gags from earlier posts; read the most recent post in `posts.js` to see what has been done.

## Recurring features

**The Slop-O-Meter Verdict.** Whenever the post critiques something (most posts do), close the critique with a verdict section: the subject, an overall rating such as "9.8/10 on the Synthetic Tapestry Scale," and three or four sub-scores under overly earnest corporate-poetic criteria ("Authenticity Resonance," "Holistic Soul Synergy"). It sits before the preachy conclusion.

**The author bio.** Sign off in italics as Julian Vance, "a flesh-and-blood wordsmith fueled by artisanal pour-over coffee, analog vinyl, and raw existential dread." Keep the name and that core line; vary the extra sentences of over-protested humanity each time.

## Length and shape

Around 700 to 1,000 words: hook, three or more H2 sections, at least one bolded-lead-in list, the Slop-O-Meter verdict, the preachy conclusion, the bio.

## Publishing

If the project root has a `posts.js` with a `window.POSTS` array, add the post there as a new entry, matching the existing entries' shape and indentation:

```js
{
    slug: "lowercase-dashed-slug",
    title: "A Dramatic Title: With a Colon and a Not-Just-X Construction",
    date: "YYYY-MM-DD",
    summary: "One or two sentences in the narrator's voice.",
    body: `
<p>...</p>
<h2>...</h2>`
}
```

- `date` is today's date. The page sorts by date, so position in the array does not matter; add the entry at the top.
- `body` is plain HTML inside a template literal: `<p>`, `<h2>`, `<ul><li>`, `<strong>`, `<em>`. No `<h1>`; the title is rendered separately. Do not use backticks or `${` inside it.
- Use typographic characters directly (— ’ “ ”), as the existing posts do.
- Leave existing posts untouched.

If there is no `posts.js`, return the post as Markdown in the conversation instead.

After publishing, tell the user the title and slug in one or two plain sentences, in your own voice, not the narrator's.
