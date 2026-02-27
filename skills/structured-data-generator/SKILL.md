---
name: structured-data-generator
description: Generate JSON-LD schema markup for GEO optimization. Use when creating structured data for articles, products, FAQs, how-to guides, organizations, and other content types to improve AI search visibility and rich results.
---

# Structured Data Generator

Generate JSON-LD schema markup to help AI search engines understand and cite your content correctly.

## Why Schema Matters for GEO

Structured data helps AI systems:
- **Parse content accurately** - Understand what the page is about
- **Extract key facts** - Pull specific data points for answers
- **Attribute correctly** - Cite your brand as the source
- **Display rich results** - Enhanced visibility in search

## Schema Types for GEO

### Article Schema

Use for: Blog posts, news articles, guides, tutorials

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Complete Guide to Generative Engine Optimization",
  "description": "Learn how to optimize content for AI search engines like ChatGPT, Perplexity, and Google AI Mode.",
  "image": "https://example.com/images/geo-guide.jpg",
  "author": {
    "@type": "Person",
    "name": "Author Name",
    "url": "https://example.com/authors/author-name",
    "jobTitle": "Content Strategist"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Company Name",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo.png",
      "width": 600,
      "height": 60
    }
  },
  "datePublished": "2024-01-15T08:00:00+00:00",
  "dateModified": "2024-03-20T10:30:00+00:00",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://example.com/geo-guide"
  },
  "keywords": ["GEO", "AI Search", "Content Optimization"],
  "articleSection": "Marketing",
  "wordCount": 2500
}
```

**Required properties:**
- `headline` - Article title
- `author` - Author information
- `datePublished` - Original publish date
- `publisher` - Publishing organization

**Recommended properties:**
- `dateModified` - Last update date (critical for AI freshness signals)
- `description` - Article summary
- `image` - Featured image
- `keywords` - Relevant terms

### FAQPage Schema

Use for: FAQ sections, Q&A pages, help documentation

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is Generative Engine Optimization (GEO)?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "GEO (Generative Engine Optimization) is the practice of optimizing content to be discovered, understood, and cited by AI search engines like ChatGPT, Perplexity, and Google AI Mode. It builds on traditional SEO by focusing on brand visibility, citation rate, and AI share of voice."
      }
    },
    {
      "@type": "Question",
      "name": "How does GEO differ from traditional SEO?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "While SEO focuses on ranking in search results and driving clicks, GEO focuses on being mentioned and cited inside AI-generated answers. GEO success is measured by brand visibility percentage, citation frequency, and share of voice in AI responses."
      }
    },
    {
      "@type": "Question",
      "name": "How often should content be updated for GEO?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "High-value pages should be refreshed every 60-90 days to maintain freshness signals. Update statistics, examples, and dates. AI engines prioritize recently updated content when generating answers."
      }
    }
  ]
}
```

**Required properties:**
- `mainEntity` - Array of Question objects
- Each Question needs `name` and `acceptedAnswer`

**Best practices:**
- Keep answers concise (40-200 words)
- Include the question keywords in the answer
- Make each answer standalone and quotable

### HowTo Schema

Use for: Tutorials, step-by-step guides, processes

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "How to Create an llms.txt File for AI Search",
  "description": "Step-by-step guide to creating an llms.txt file that helps AI crawlers discover and understand your content.",
  "image": "https://example.com/images/llms-txt-guide.jpg",
  "totalTime": "PT15M",
  "estimatedCost": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": "0"
  },
  "supply": [
    {
      "@type": "HowToSupply",
      "name": "Text editor"
    },
    {
      "@type": "HowToSupply",
      "name": "Web hosting access"
    }
  ],
  "tool": [
    {
      "@type": "HowToTool",
      "name": "Code editor (VS Code, Cursor)"
    }
  ],
  "step": [
    {
      "@type": "HowToStep",
      "name": "Audit your content",
      "text": "Identify your most important pages: documentation, pricing, policies, and key product pages.",
      "url": "https://example.com/llms-txt-guide#step1",
      "image": "https://example.com/images/step1.jpg"
    },
    {
      "@type": "HowToStep",
      "name": "Create the file structure",
      "text": "Create a new file named llms.txt at your domain root. Start with your brand name as H1 and a blockquote description.",
      "url": "https://example.com/llms-txt-guide#step2"
    },
    {
      "@type": "HowToStep",
      "name": "Add content sections",
      "text": "Organize links into sections like Docs, Product, Support, and Optional. Include brief descriptions for each link.",
      "url": "https://example.com/llms-txt-guide#step3"
    },
    {
      "@type": "HowToStep",
      "name": "Deploy and test",
      "text": "Upload the file and verify it's accessible at https://yourdomain.com/llms.txt. Test by asking AI assistants about your product.",
      "url": "https://example.com/llms-txt-guide#step4"
    }
  ]
}
```

**Required properties:**
- `name` - Title of the how-to
- `step` - Array of HowToStep objects

### Product Schema

Use for: Product pages, SaaS offerings, e-commerce

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Superlines Analytics Platform",
  "description": "AI Search Intelligence platform that helps brands track, optimize, and grow their visibility in AI Search across ChatGPT, Perplexity, Gemini, and Google AI Mode.",
  "image": "https://superlines.io/images/product.jpg",
  "brand": {
    "@type": "Brand",
    "name": "Superlines"
  },
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "99",
    "highPrice": "499",
    "priceCurrency": "EUR",
    "offerCount": "3",
    "offers": [
      {
        "@type": "Offer",
        "name": "Starter",
        "price": "99",
        "priceCurrency": "EUR",
        "priceValidUntil": "2025-12-31",
        "availability": "https://schema.org/InStock"
      },
      {
        "@type": "Offer",
        "name": "Professional",
        "price": "299",
        "priceCurrency": "EUR",
        "priceValidUntil": "2025-12-31",
        "availability": "https://schema.org/InStock"
      },
      {
        "@type": "Offer",
        "name": "Enterprise",
        "price": "499",
        "priceCurrency": "EUR",
        "priceValidUntil": "2025-12-31",
        "availability": "https://schema.org/InStock"
      }
    ]
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "127"
  }
}
```

### Organization Schema

Use for: Company pages, about pages, homepage

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Superlines",
  "alternateName": "Superlines.io",
  "url": "https://superlines.io",
  "logo": "https://superlines.io/logo.png",
  "description": "AI Search Intelligence platform for enterprises and agencies.",
  "foundingDate": "2023",
  "founders": [
    {
      "@type": "Person",
      "name": "Founder Name"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Helsinki",
    "addressCountry": "FI"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "contactType": "customer service",
    "url": "https://superlines.io/contact"
  },
  "sameAs": [
    "https://www.linkedin.com/company/superlines",
    "https://twitter.com/superlines"
  ]
}
```

### BreadcrumbList Schema

Use for: Navigation paths on any page

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://example.com"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Articles",
      "item": "https://example.com/articles"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "GEO Guide",
      "item": "https://example.com/articles/geo-guide"
    }
  ]
}
```

## Implementation Guide

### HTML Placement

Place JSON-LD in the `<head>` section:

```html
<head>
  <title>Page Title</title>
  <meta name="description" content="...">
  
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Article",
    ...
  }
  </script>
</head>
```

### Multiple Schema Types

You can include multiple schema types on one page:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "name": "Company Name",
      ...
    },
    {
      "@type": "WebPage",
      "name": "Page Title",
      ...
    },
    {
      "@type": "Article",
      "headline": "Article Title",
      ...
    }
  ]
}
</script>
```

## Validation Checklist

Before deploying schema markup:

- [ ] JSON syntax is valid (no trailing commas, proper quotes)
- [ ] All required properties are present
- [ ] URLs are absolute (include https://)
- [ ] Dates use ISO 8601 format (2024-01-15T08:00:00+00:00)
- [ ] Text values are properly escaped
- [ ] Images are valid URLs and accessible
- [ ] Schema type matches content type
- [ ] No duplicate conflicting schema on same page

## Testing Tools

1. **Google Rich Results Test** - https://search.google.com/test/rich-results
2. **Schema.org Validator** - https://validator.schema.org/
3. **JSON-LD Playground** - https://json-ld.org/playground/

## Quick Reference Table

| Content Type | Schema | Key Properties |
|--------------|--------|----------------|
| Blog/Article | Article | headline, author, datePublished, dateModified |
| FAQ | FAQPage | mainEntity (Questions with Answers) |
| Tutorial | HowTo | name, step (HowToSteps) |
| Product | Product | name, offers, brand |
| Company | Organization | name, url, logo, description |
| Navigation | BreadcrumbList | itemListElement (ListItems) |
| Person | Person | name, jobTitle, url |
| Service | Service | name, provider, description |
