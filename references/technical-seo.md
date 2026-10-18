# Technical SEO and crawler access

Read this when a recommendation genuinely depends on how the site is built: crawl access, indexing, canonicalization, international publishing, structured data or performance.

Everything here can be verified by inspecting the site or reading the platform's current documentation. None of it predicts rankings or citations, and none of it rescues a blog that has nothing worth reading.

## Before recommending anything technical

- Inspect the live site and record what you inspected, when, and what you could not reach.
- Check current platform documentation instead of recalled practice; this area changes faster than most.
- Describe a technical change as a hypothesis with a plausible mechanism, never as a promised outcome.
- If the site is not yours to change, write the recommendation for whoever owns it, with the reason, the cost and the trade-off.

## Crawl access and AI answer engines

Whether answer engines may read the blog is an editorial and business decision, and it is one of the few technical settings that changes what AI systems are able to say about the project.

- Name the agents explicitly in `robots.txt`. The ones that matter most today are `GPTBot`, `ClaudeBot`, `PerplexityBot` and `Google-Extended`. The list grows, so re-check it rather than trusting this paragraph.
- Allowing a crawler is what makes retrieval and citation possible. Blocking it removes the content from those answers and, depending on the agent, from model training as well.
- `Google-Extended` is a separate control from Google Search indexing. A site can stay fully indexed in Search while opting out of use in Google's generative products.
- Record the decision and its date somewhere durable, or it gets re-argued every quarter and the default quietly drifts.

## Indexing and canonicalization

- One canonical URL per article, declared explicitly, including on syndicated or republished copies.
- Check that tag, category, paginated and filtered archive pages do not compete with the articles they list.
- Keep drafts, noindexed pages and thin archives out of the sitemap, and keep every published article in it.

## Metadata

- Title: unique, roughly 50–60 characters, carrying the reader's question or the promise.
- Description: unique, roughly 150–160 characters, written as a sentence a person would actually click.
- Open Graph for anything that will be shared: title, description, image, canonical URL and type.
- Emit a real publication date and a real modification date. Move the modification date only on a substantive revision; changing it without changing the content is detectable and counterproductive.

## International publishing

When the blog publishes in more than one language or region, declare the variants with `hreflang`, include `x-default`, and keep them consistent between the page and the sitemap. A single-language blog has no work to do here, and should not be given this task.

## Structured data

- Choose the types the page actually is: `Article`, `BreadcrumbList`, `Organization`, `Person` for the author, and `FAQPage` only where real question-and-answer content is on the page.
- Combine several types with `@graph` under one `@context`.
- Generate it from the fields the article already carries. Hand-writing structured data beside a pipeline that also emits it creates two versions of the truth.
- Worth stating plainly: structured data describes the page. It is not a guaranteed ranking factor and not a precondition for being quoted.

## Performance

Core Web Vitals thresholds as currently published: largest contentful paint under 2.5 seconds, interaction to next paint under 200 milliseconds, cumulative layout shift under 0.1.

An editor controls more of this than it looks. Oversized uncompressed hero images, autoplaying embeds, and images or ads without reserved dimensions are the usual causes, and all three are content decisions rather than engineering ones.

## What is observable about answer surfaces

- Search Console reports impressions and clicks for AI Overviews where the platform exposes them.
- Referral traffic from assistants shows up as a source, though attribution is imperfect and a good share arrives unattributed.
- Asking an assistant about the project's topic, and about the brand plus a phrase such as "according to", shows what is being repeated.
- Keep these as first-party observations, separated from inference as everywhere else in this skill. One appearance in one answer is an anecdote, not a trend, and no measurement here establishes cause.
