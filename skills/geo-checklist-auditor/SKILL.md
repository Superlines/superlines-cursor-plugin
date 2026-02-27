---
name: geo-checklist-auditor
description: Audit pages against the GEO best practices checklist. Use when reviewing content for AI search readiness, ensuring pages follow Generative Engine Optimization principles, or preparing content for better visibility in ChatGPT, Perplexity, and Google AI Mode.
---

# GEO Checklist Auditor

Audit web pages against the comprehensive GEO (Generative Engine Optimization) best practices checklist to ensure optimal visibility in AI search engines.

## The 10-Point GEO Audit Checklist

Use this checklist as a comprehensive pass before publishing or updating any high-value page.

### 1. AI Search Visibility Baseline

**What to check:**
- Has the page topic been tested in AI assistants?
- Which brands currently appear for related queries?
- What sources are being cited?

**Audit actions:**
- [ ] Test 3-5 relevant prompts in ChatGPT
- [ ] Test same prompts in Perplexity
- [ ] Test in Google AI Mode if available
- [ ] Document which competitors are mentioned
- [ ] Note which sources are cited

**Questions to ask AI:**
```
"What are the best [your category]?"
"How does [your product type] work?"
"[Your product] vs [competitor] comparison"
"What companies offer [your service]?"
```

### 2. Prompt-to-Intent Mapping

**What to check:**
- Does content address real user prompts?
- Are all funnel stages covered?
- Do headings match query patterns?

**Audit criteria:**
- [ ] Awareness prompts addressed (what is X, how does X work)
- [ ] Consideration prompts addressed (best X for Y, X vs Z)
- [ ] Decision prompts addressed (X pricing, X review, buy X)
- [ ] H2 headings match real question patterns
- [ ] Content covers query fan-out variations

**Funnel mapping table:**

| Stage | Prompt Pattern | Page Addresses? |
|-------|---------------|-----------------|
| Awareness | "What is [topic]?" | ☐ Yes ☐ No |
| Awareness | "How does [topic] work?" | ☐ Yes ☐ No |
| Consideration | "Best [category] for [use case]" | ☐ Yes ☐ No |
| Consideration | "[Product A] vs [Product B]" | ☐ Yes ☐ No |
| Decision | "[Product] pricing" | ☐ Yes ☐ No |
| Decision | "[Product] reviews" | ☐ Yes ☐ No |

### 3. Cornerstone Content Quality

**What to check:**
- Is content authoritative and comprehensive?
- Are claims supported by evidence?
- Is expertise demonstrated?

**Audit criteria:**
- [ ] Content length appropriate (1,500+ words for guides)
- [ ] Clear definitions provided for key terms
- [ ] Real examples and case studies included
- [ ] Data/statistics from credible sources
- [ ] Expert quotes or citations where relevant
- [ ] Author credentials visible
- [ ] Original insights not found elsewhere

**Quality indicators:**
| Element | Present? | Quality (1-5) |
|---------|----------|---------------|
| Definitions | ☐ | ___ |
| Examples | ☐ | ___ |
| Data/Statistics | ☐ | ___ |
| Expert quotes | ☐ | ___ |
| Original research | ☐ | ___ |

### 4. Extractability and Structure

**What to check:**
- Can AI easily extract key information?
- Is content structured for machine reading?
- Does formatting support quotability?

**Audit criteria:**

**Page structure:**
- [ ] Clear H1 matching primary intent
- [ ] Logical H2/H3 hierarchy
- [ ] TL;DR or summary section at top
- [ ] Key takeaways section
- [ ] FAQ section with common questions

**Content formatting:**
- [ ] Short paragraphs (3-4 sentences max)
- [ ] Bullet lists for features/benefits
- [ ] Numbered lists for steps/processes
- [ ] Tables for comparisons/specifications
- [ ] Each paragraph is quotable standalone

**Technical extractability:**
- [ ] Page loads in < 0.4 seconds (FCP target)
- [ ] Content in initial HTML (not JS-rendered)
- [ ] Clean semantic HTML structure

### 5. Schema and Metadata

**What to check:**
- Is appropriate schema markup present?
- Are meta tags optimized?
- Is structured data valid?

**Schema audit:**
- [ ] Schema type matches content (Article, FAQPage, HowTo, Product)
- [ ] Required properties populated
- [ ] dateModified reflects actual last update
- [ ] JSON-LD syntax is valid
- [ ] No conflicting schema on page

**Metadata audit:**
- [ ] Title is descriptive (< 60 characters)
- [ ] Meta description summarizes content (150-160 chars)
- [ ] Canonical URL is correct
- [ ] Open Graph tags present
- [ ] Language declared

**Schema checklist by content type:**

| Content Type | Required Schema | Present? | Valid? |
|--------------|-----------------|----------|--------|
| Article/Blog | Article | ☐ | ☐ |
| FAQ page | FAQPage | ☐ | ☐ |
| Tutorial | HowTo | ☐ | ☐ |
| Product page | Product | ☐ | ☐ |
| Company page | Organization | ☐ | ☐ |

### 6. Web-Wide Footprint

**What to check:**
- Does brand appear on third-party sources?
- Are key directories and platforms covered?
- Is information consistent across sources?

**Third-party presence audit:**
- [ ] Wikipedia/Wikidata (if notable)
- [ ] Industry directories
- [ ] Review sites (G2, Capterra, Trustpilot)
- [ ] LinkedIn company page
- [ ] Relevant Reddit communities
- [ ] YouTube presence
- [ ] Industry forums/communities

**Consistency check:**
- [ ] Company description consistent across platforms
- [ ] Product information matches website
- [ ] Pricing is current everywhere
- [ ] Contact information is accurate

### 7. Brand Authority and Engagement

**What to check:**
- Is content publishing consistent?
- Are there quality backlinks?
- Is brand being discussed?

**Authority indicators:**
- [ ] Regular content publishing cadence
- [ ] Quality external links to content
- [ ] Media mentions/press coverage
- [ ] Customer reviews and testimonials
- [ ] Social engagement on content
- [ ] Industry awards or recognition

### 8. GEO Metrics Tracking

**What to check:**
- Are AI visibility metrics being tracked?
- Can improvements be measured?

**Metrics to establish:**
- [ ] Brand Visibility baseline (% of answers mentioning brand)
- [ ] Citation Rate baseline (% of answers citing domain)
- [ ] AI Share of Voice vs competitors
- [ ] Human vs bot traffic tracked
- [ ] AI referral traffic identified

### 9. Content Freshness

**What to check:**
- Is content regularly updated?
- Are dates accurate and visible?

**Freshness audit:**
- [ ] Last update date is visible
- [ ] Statistics are current (< 12 months old)
- [ ] Examples are relevant and recent
- [ ] Links are working (no 404s)
- [ ] Product information is accurate
- [ ] Pricing is current

**Recommended refresh cadence:**

| Content Type | Refresh Every |
|--------------|---------------|
| Product pages | Monthly |
| Pricing pages | Monthly |
| Industry guides | 60-90 days |
| Blog posts with data | Quarterly |
| Documentation | When features change |
| Evergreen content | 6 months |

### 10. Common GEO Mistakes Check

**Verify the page avoids these issues:**
- [ ] NOT relying on thin content (< 500 words for important pages)
- [ ] NOT keyword stuffing unnaturally
- [ ] NOT using only one distribution channel
- [ ] NOT measuring only Google metrics
- [ ] NOT ignoring AI bot access in robots.txt
- [ ] NOT using JavaScript-only content rendering
- [ ] NOT having slow page load times
- [ ] NOT missing schema markup
- [ ] NOT having inconsistent brand information
- [ ] NOT neglecting third-party presence

## Audit Scoring

### Calculate Overall GEO Score

| Section | Max Points | Score |
|---------|------------|-------|
| 1. Visibility Baseline | 10 | ___ |
| 2. Prompt Mapping | 10 | ___ |
| 3. Content Quality | 10 | ___ |
| 4. Extractability | 10 | ___ |
| 5. Schema/Metadata | 10 | ___ |
| 6. Web-Wide Footprint | 10 | ___ |
| 7. Brand Authority | 10 | ___ |
| 8. Metrics Tracking | 10 | ___ |
| 9. Content Freshness | 10 | ___ |
| 10. Mistakes Avoided | 10 | ___ |
| **Total** | **100** | **___** |

### Score Interpretation

| Score | Rating | Action |
|-------|--------|--------|
| 90-100 | Excellent | Maintain and monitor |
| 75-89 | Good | Minor optimizations needed |
| 60-74 | Fair | Significant improvements needed |
| 40-59 | Poor | Major restructuring required |
| < 40 | Critical | Full content overhaul needed |

## Audit Report Template

```markdown
# GEO Audit Report

**Page:** [URL]
**Date:** [Date]
**Auditor:** [Name]
**Overall Score:** [X/100]

## Executive Summary
[2-3 sentence summary of findings]

## Critical Issues (Fix Immediately)
1. [Issue with impact]
2. [Issue with impact]

## High Priority (Fix This Week)
1. [Issue with recommendation]
2. [Issue with recommendation]

## Medium Priority (Fix This Month)
1. [Issue with recommendation]
2. [Issue with recommendation]

## Strengths
- [What's working well]
- [What's working well]

## Recommendations
1. [Specific actionable recommendation]
2. [Specific actionable recommendation]
3. [Specific actionable recommendation]

## Next Review Date
[Date for follow-up audit]
```

## Quick Audit Checklist

For fast assessments, use this condensed checklist:

- [ ] **Structure:** H1 matches intent, logical H2/H3 hierarchy
- [ ] **Answer First:** Main point in first 1-2 sentences
- [ ] **TL;DR:** Summary section at page top
- [ ] **FAQ:** Common questions addressed
- [ ] **Schema:** Appropriate type, valid syntax
- [ ] **Speed:** Page loads under 0.4s FCP
- [ ] **Freshness:** Updated within 90 days
- [ ] **Entities:** Consistent terminology throughout
- [ ] **Evidence:** Claims backed by data/sources
- [ ] **Quotability:** Each paragraph stands alone
