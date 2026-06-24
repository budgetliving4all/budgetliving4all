# Budget Living 4 All - Writing Style Guide

This document covers how articles on this site should be written and what to avoid. Follow it for every article, every section, every sentence.

---

## The goal

Write like someone who actually knows the subject explaining it to a friend. Not a blog post. Not a content marketing piece. Not something that sounds like it was generated and lightly edited. If a sentence would feel out of place in a normal conversation, rewrite it.

Readers are practical people looking for information that works. They are not looking for reassurance, enthusiasm, or to be told how useful this article is going to be.

---

## What to never use

### Punctuation and formatting
- No em dashes (—). Use a comma, a period, or restructure the sentence.
- No ellipsis for effect (...). Fine in quoted speech, not in prose.
- No exclamation points. If something is important, the writing makes it clear.
- No ALL CAPS for emphasis. Use bold sparingly if something truly needs to stand out.

### Sentence patterns that signal AI writing
These constructions appear constantly in AI-generated content. Avoid all of them.

- "It's not X, it's Y" framing ("It's not about perfection, it's about progress")
- "The truth is..." / "Here's the thing..." / "The reality is..."
- "It's worth noting that..."
- "At the end of the day..."
- "When it comes to..."
- "In this article, you'll learn..." and any other throat-clearing intros
- "Let's dive in" or any variation
- Rhetorical questions to open sections ("But what does that actually mean?")
- "Simply" / "easily" / "just" used to make something sound effortless
- "Essentially" / "basically" / "truly" / "really" as filler
- "This means that..." to start a sentence
- "One thing to keep in mind is..."
- "Needless to say..."
- Wrapping up with "In conclusion" or "To summarize"

### Honesty signals that undermine themselves
Do not tell people you are being honest. Do not flag that a caveat is coming. Do not announce that a recommendation is genuine. If the writing is honest, it shows.

Avoid:
- "One honest caveat worth knowing..."
- "To be transparent..."
- "I want to be upfront that..."
- "Genuinely" / "honestly" used to preface a claim

Just say the thing.

### Overclaiming
Do not promise results that are not guaranteed. Do not say something "works" or "solves" a problem when it helps with it. Do not say something is "the best" without data to back it up.

Bad: "This routine will transform your mornings."
Better: "This routine cuts morning prep time significantly for most people."

Do not tell people they "will" feel a certain way or "won't" notice something. You do not know that.

Bad: "You'll barely notice you're eating the same food."
Better: "Rotating sauces helps, but it is not going to make the same food taste like something completely different. The goal is making the routine sustainable, not making it feel new every day."

---

## Structure

### Intros
Get to the point in the first paragraph. Explain what the article covers and who it is for. Do not spend three paragraphs building up to the topic.

Bad intro: "Meal prep has become one of the most popular trends in the health and wellness space. More and more people are discovering that spending a few hours in the kitchen each week can lead to..."

Better: "Most meal prep content assumes you're cooking for a family. If you're cooking for yourself, most of it doesn't apply."

### Headings
Make headings descriptive and plain. They should tell the reader what is in the section, not tease it.

Bad: "Why this matters"
Better: "How long prepped food keeps"

Bad: "The secret to saving money on groceries"
Better: "Where the biggest grocery savings come from"

### Lists
Use lists for genuinely list-like things: steps, ingredients, options. Do not turn every point into a bullet. Paragraphs can handle three related ideas without needing bullet points.

Keep bullets parallel. If one starts with a verb, they all start with a verb.

### Length
Write as long as the topic requires. Do not pad to hit a word count. Do not cut useful information to stay short. 1,200-1,800 words is a reasonable target for most articles, but follow the content, not the number.

---

## Tone

### Direct
Say what you mean. If something has a downside, say so. If the evidence is mixed, say so. If something only works for some people, say so.

### Neutral on preference
Do not push one approach as universally correct. People have different schedules, budgets, living situations, and cooking abilities. Where something depends on circumstances, acknowledge that.

### Not motivational
This is not a self-help site. Do not tell people they can do it, that small steps matter, or that progress is what counts. Just give them the information.

---

## Food safety

Every article that involves cooking must include food safety information sourced from government sources. This is not optional.

- Internal temperatures: always from FoodSafety.gov
- Storage times: always from FoodSafety.gov Cold Food Storage Chart
- Use the `{% include safe-temp.html food="[type]" %}` include wherever cooking is described
- Never state a safety figure without linking to the source

---

## Prices and cost data

- Always use `{% include price-note.html date="[Month Year]" %}` above any price table
- Link to USDA ERS and BLS data inline when citing price trends
- State when prices were checked
- Tell readers to verify locally - prices vary significantly by region
- Never present a price as fixed or definitive

---

## Product recommendations

Every product recommended must meet these minimums before going in an article:

- At least 1,000 Amazon reviews
- 4.0 stars or higher
- Currently in stock

In the product write-up:
- State the star rating and review count
- Describe what it does
- Include any common complaints or limitations from reviews
- Do not hide negatives

Do not say a product is "worth every penny" or "a game changer." Describe what it does and let the reader decide.

Affiliate link format: `https://www.amazon.com/dp/[ASIN]?tag=budgetliving4-20`

---

## The affiliate disclosure

Every article with affiliate links gets this at the very top of the article body, before any other content:

```
<p class="affiliate-notice"><strong>Heads up:</strong> Some links here are affiliate links. We earn a small commission if you buy through them, at no cost to you. We only link to products we'd actually recommend.</p>
```

---

## Sources

Every article ends with a sources line that links to every government or data source cited in the article. Format:

```
*Sources: [Name](URL) · [Name](URL) · [Note about prices or product data as applicable.]*
```

Include last-reviewed dates for government sources where available.

---

## Final check before publishing

Read the article out loud. If any sentence sounds like something a content generator would write, rewrite it. If any claim does not have a source, add one or remove the claim. If any price or product detail has not been verified recently, verify it.
