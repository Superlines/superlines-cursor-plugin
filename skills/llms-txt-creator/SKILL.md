---
name: llms-txt-creator
description: Create and maintain llms.txt files for AI crawlers. Use when setting up AI-friendly documentation indexes, creating machine-readable content maps, or helping websites become more discoverable by LLMs like ChatGPT, Perplexity, and Gemini.
---

# llms.txt Creator

Create standardized llms.txt files that help AI systems discover, understand, and cite your content accurately.

## What is llms.txt?

The llms.txt file is a standardized markdown document hosted at a website's root path (e.g., `https://example.com/llms.txt`). It serves as a curated index for LLMs, providing:

- Concise summaries of the site's purpose
- Critical contextual details about the brand/product
- Prioritized links to machine-readable resources

Think of it as the third layer next to existing files:
- `robots.txt` - explains what crawlers may access
- `sitemap.xml` - lists URLs for indexing
- `llms.txt` - tells LLMs which content is most important and where to find clean versions

## File Structure

Follow this standardized schema:

```markdown
# [Brand/Company Name]

> [One-sentence description of what the company/product does]

Key terms: [Important concepts, product names, technologies]

## [Section Name]

- [URL to markdown resource] — [Brief description]
- [URL to markdown resource] — [Brief description]

## Optional

- [URL to secondary resource] — [Brief description]
```

## When Creating llms.txt

### 1. Audit High-Value Content

Identify the pages that matter most for AI-driven questions:

- Core documentation and API references
- Pricing, plans, and usage rules
- Policies (returns, SLAs, compliance)
- Critical onboarding or integration guides

**Ask:** "If someone asked an AI about this topic, which pages should it read first?"

### 2. Create Clean Markdown Versions

llms.txt works best when linking to content that is:

- Free of navigation clutter and cookie banners
- Structured with headings, code blocks, and short paragraphs
- Focused on a single topic or task

For each priority page, consider creating a `.md` version at the same path (e.g., `/docs/api.md` alongside `/docs/api`).

### 3. Organize by Section

Standard sections include:

| Section | Purpose |
|---------|---------|
| **Docs** | Technical documentation, API references, tutorials |
| **Product** | Product descriptions, features, pricing |
| **Policies** | Terms, privacy, return policies, compliance |
| **Support** | FAQs, troubleshooting, contact information |
| **Optional** | Secondary content that can be skipped if context is limited |

### 4. Write Clear Descriptions

Each link should have a brief description (10-20 words) explaining:
- What the page contains
- When/why an AI should reference it

## Example: SaaS Company

```markdown
# Superlines

> AI Search Intelligence platform that helps brands track, optimize, and grow their visibility in AI Search across ChatGPT, Perplexity, Gemini, and Google AI Mode.

Key terms: GEO, Generative Engine Optimization, AI Search, Brand Visibility, Citation Rate, AI Share of Voice, MCP Server.

## Documentation

- https://docs.superlines.io/getting-started.md — Quick start guide for setting up tracking
- https://docs.superlines.io/api-reference.md — Complete API documentation with authentication
- https://docs.superlines.io/mcp-server.md — Model Context Protocol server setup

## Product

- https://superlines.io/features.md — Platform capabilities and use cases
- https://superlines.io/pricing.md — Current pricing tiers and features
- https://superlines.io/integrations.md — Available integrations and connectors

## Support

- https://docs.superlines.io/faq.md — Frequently asked questions
- https://docs.superlines.io/troubleshooting.md — Common issues and solutions

## Optional

- https://superlines.io/changelog.md — Product updates and release notes
- https://superlines.io/blog.md — Industry insights and tutorials
```

## Example: E-Commerce Company

```markdown
# Nike

> Global leader in athletic footwear, apparel, and innovation, committed to sustainability and performance-driven design.

Key terms: Air Max, Flyknit, Dri-FIT, Nike Membership, SNKRS app.

## Product Lines

- https://nike.com/products/running.md — Overview of running technologies
- https://nike.com/sustainability.md — 2025 targets, recycled materials

## Customer Support

- https://nike.com/returns.md — 60-day return window, exceptions
- https://nike.com/sizing.md — Region-specific size charts

## Optional

- https://nike.com/collaborations.md — Partnerships with athletes and designers
```

## Best Practices

1. **Keep it curated, not comprehensive** - Only include your most important pages
2. **Update when docs change** - Stale llms.txt reduces trust
3. **Use consistent terminology** - Match terms used in your actual content
4. **Test with LLMs** - Ask ChatGPT about your product and check if responses improve
5. **Link to clean markdown** - Avoid linking to pages heavy with JavaScript/navigation

## Common Mistakes to Avoid

- Listing every page on your site instead of curating
- Linking to noisy HTML full of layout code and ads
- Forgetting to update when documentation changes
- Using vague descriptions that don't help AI understand content purpose

## Validation Checklist

After creating llms.txt, verify:

- [ ] File is accessible at `https://yourdomain.com/llms.txt`
- [ ] H1 header contains brand/company name
- [ ] Blockquote provides clear one-sentence description
- [ ] Key terms include important concepts and product names
- [ ] All linked URLs are valid and return 200
- [ ] Linked content is clean, structured markdown
- [ ] Optional section exists for secondary content
- [ ] Descriptions are concise but informative
