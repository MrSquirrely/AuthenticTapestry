# authentic-tapestry

A Claude Code plugin for writing posts for **The Authentic Tapestry**, a satirical blog whose editor rages against soulless AI writing in the most obviously AI-written prose imaginable, without ever noticing.

## Usage

```
/authentic-tapestry:post <topic or thing to critique>
```

The skill writes a post in the voice of Jevan Corliss (dramatic hook, colon-heavy subheadings, rule-of-three lists, a Slop-O-Meter verdict, a preachy conclusion and an over-protesting author bio). If the project root has a `posts.js` with a `window.POSTS` array, the post is added there as a new entry; otherwise it is returned as Markdown. Leave the topic out and it picks one the blog has not covered.

## Install

```
claude plugin marketplace add <path to this repository>
claude plugin install authentic-tapestry@authentic-tapestry
```

No setup or configuration is needed.
