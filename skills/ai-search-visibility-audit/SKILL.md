---
name: ai-search-visibility-audit
description: Comprehensive AI search visibility analysis using Superlines data. Use when auditing brand visibility across AI engines, analyzing competitor presence, or building GEO strategies based on real AI search data. Requires Superlines MCP server connection.
---

# AI Search Visibility Audit

Perform comprehensive AI search visibility analysis using real-time data from AI search engines. This skill leverages the Superlines MCP server for authentic visibility metrics.

## Prerequisites

This skill requires the **Superlines MCP server** to access AI search visibility data.

### Installing Superlines MCP Server

Add the Superlines MCP server to your configuration:

**For Claude Code** (`~/.claude.json` or project `.claude.json`):
```json
{
  "mcpServers": {
    "superlines": {
      "command": "npx",
      "args": ["@superlines/mcp-server"],
      "env": {
        "SUPERLINES_API_KEY": "your-api-key"
      }
    }
  }
}
```

**For Cursor** (`.cursor/mcp.json`):
```json
{
  "mcpServers": {
    "superlines": {
      "command": "npx",
      "args": ["@superlines/mcp-server"],
      "env": {
        "SUPERLINES_API_KEY": "your-api-key"
      }
    }
  }
}
```

Get your API key at [superlines.io](https://superlines.io).

## Visibility Audit Framework

### Step 1: Define Audit Scope

Before running the audit, define:

**Brand Information:**
- Primary brand name
- Alternative names/spellings
- Key products/services
- Target markets

**Competitor Set:**
- 3-5 direct competitors
- 2-3 indirect competitors (optional)

**Topic Clusters:**
- Primary category queries
- Product-specific queries
- Comparison queries
- How-to/educational queries

### Step 2: Collect Visibility Data

Use Superlines MCP tools to gather data:

```
# Get brand visibility across AI engines
superlines.get_brand_visibility({
  brand: "Your Brand",
  engines: ["chatgpt", "perplexity", "gemini", "google-ai-mode"],
  date_range: "last_30_days"
})

# Get competitor analysis
superlines.get_competitor_analysis({
  brand: "Your Brand",
  competitors: ["Competitor A", "Competitor B", "Competitor C"],
  topics: ["your category", "key feature"]
})

# Get citation analysis
superlines.get_citations({
  domain: "yourdomain.com",
  date_range: "last_30_days"
})
```

### Step 3: Analyze Key Metrics

#### Brand Visibility Score

**Definition:** Percentage of AI answers that mention your brand for tracked queries.

**Benchmarks:**
| Visibility | Rating | Interpretation |
|------------|--------|----------------|
| > 30% | Excellent | Strong AI presence |
| 20-30% | Good | Solid foundation |
| 10-20% | Fair | Room for improvement |
| < 10% | Poor | Significant gap |

#### Citation Rate

**Definition:** Percentage of answers that cite your domain as a source.

**Benchmarks:**
| Citation Rate | Rating | Interpretation |
|---------------|--------|----------------|
| > 20% | Excellent | Trusted source |
| 10-20% | Good | Building authority |
| 5-10% | Fair | Limited trust |
| < 5% | Poor | Not seen as authoritative |

#### AI Share of Voice

**Definition:** Your brand mentions divided by total competitor mentions.

**Calculation:**
```
AI SOV = (Your Mentions / Total Category Mentions) × 100
```

**Benchmarks:**
| Share of Voice | Rating | Position |
|----------------|--------|----------|
| > 25% | Leader | Category leader |
| 15-25% | Strong | Major player |
| 5-15% | Moderate | Competitive |
| < 5% | Weak | Visibility gap |

#### Context Accuracy

**Definition:** Whether AI describes your brand correctly.

**Check for:**
- Correct product descriptions
- Accurate pricing information
- Current feature lists
- Proper brand positioning
- No outdated information

### Step 4: Gap Analysis

#### Visibility Gaps

Identify where competitors appear but you don't:

```
# Query gap analysis
superlines.get_query_gaps({
  brand: "Your Brand",
  competitors: ["Competitor A", "Competitor B"],
  threshold: 0.2  # Show queries where competitors have 20%+ visibility
})
```

**Gap categories:**
1. **Complete absence** - You never appear
2. **Weak presence** - You appear < 10% vs competitor > 30%
3. **Competitive** - Similar visibility
4. **Leadership** - You dominate

#### Citation Source Gaps

Identify where competitors are cited but you're not:

```
# Citation source analysis
superlines.get_citation_sources({
  competitors: ["Competitor A", "Competitor B"],
  show_gaps: true
})
```

**Common citation sources:**
- Industry publications
- Review sites (G2, Capterra)
- Wikipedia
- Reddit discussions
- YouTube videos
- LinkedIn articles

### Step 5: Query Fan-Out Analysis

Understand how AI systems expand user queries:

```
# Get query fan-out data
superlines.get_query_fanout({
  primary_query: "best GEO tools",
  engine: "chatgpt"
})
```

**What to analyze:**
- Which sub-queries does AI generate?
- Does your content address these sub-queries?
- Are competitors better positioned for fan-out queries?

**Example fan-out:**
```
Primary: "best GEO tools"
├── "GEO analytics platforms"
├── "AI search visibility software"
├── "ChatGPT ranking tools"
├── "Superlines vs competitors"
└── "GEO tool pricing comparison"
```

### Step 6: Engine-by-Engine Analysis

Compare performance across different AI engines:

| Engine | Your Visibility | Top Competitor | Gap |
|--------|-----------------|----------------|-----|
| ChatGPT | _% | _% | _% |
| Perplexity | _% | _% | _% |
| Gemini | _% | _% | _% |
| Google AI Mode | _% | _% | _% |
| Claude | _% | _% | _% |

**Engine-specific notes:**
- **ChatGPT:** Highest search volume, uses Bing/web search
- **Perplexity:** Heavy citation focus, shows sources prominently
- **Gemini:** Integrated with Google Search, affects AI Overviews
- **Google AI Mode:** Uses Google index, affects traditional search too

## Audit Report Template

### AI Search Visibility Audit Report

```markdown
# AI Search Visibility Audit
**Brand:** [Brand Name]
**Date:** [Date]
**Period:** [Date Range]

## Executive Summary
[2-3 paragraph summary of key findings]

## Key Metrics

| Metric | Current | Previous | Change | Target |
|--------|---------|----------|--------|--------|
| Brand Visibility | X% | X% | +/-X% | X% |
| Citation Rate | X% | X% | +/-X% | X% |
| AI Share of Voice | X% | X% | +/-X% | X% |
| Context Accuracy | X% | X% | +/-X% | 95%+ |

## Visibility by Engine

| Engine | Visibility | Citations | SOV Rank |
|--------|------------|-----------|----------|
| ChatGPT | X% | X | #X |
| Perplexity | X% | X | #X |
| Gemini | X% | X | #X |
| Google AI Mode | X% | X | #X |

## Competitor Analysis

| Competitor | Visibility | Citation Rate | SOV |
|------------|------------|---------------|-----|
| Competitor A | X% | X% | X% |
| Competitor B | X% | X% | X% |
| Competitor C | X% | X% | X% |
| **Your Brand** | **X%** | **X%** | **X%** |

## Top Visibility Gaps

1. **[Query/Topic]**
   - Your visibility: X%
   - Top competitor: X% (Competitor A)
   - Opportunity: [Description]

2. **[Query/Topic]**
   - Your visibility: X%
   - Top competitor: X% (Competitor B)
   - Opportunity: [Description]

## Citation Source Analysis

**Currently citing your brand:**
- [Source 1] - [X citations]
- [Source 2] - [X citations]

**Citing competitors but not you:**
- [Source 1] - Cites: [Competitor A, B]
- [Source 2] - Cites: [Competitor A]

## Context Accuracy Issues

- [ ] [Issue 1: e.g., "Outdated pricing mentioned"]
- [ ] [Issue 2: e.g., "Missing key product feature"]

## Recommendations

### Immediate Actions (This Week)
1. [Specific action with expected impact]
2. [Specific action with expected impact]

### Short-Term (This Month)
1. [Specific action with expected impact]
2. [Specific action with expected impact]

### Medium-Term (This Quarter)
1. [Specific action with expected impact]
2. [Specific action with expected impact]

## Appendix

### Tracked Queries
[List of queries being monitored]

### Data Sources
[Superlines platform, date range, methodology]
```

## Action Planning

Based on audit findings, prioritize actions:

### Quick Wins (1-2 weeks)
- Update outdated content on high-visibility pages
- Fix context accuracy issues
- Add missing schema markup
- Refresh dates on cornerstone content

### Medium Priority (1-3 months)
- Create content for visibility gap topics
- Build presence on citation source sites
- Develop comparison content
- Expand FAQ coverage

### Strategic Initiatives (3-6 months)
- Build third-party authority (PR, partnerships)
- Develop original research/data
- Create comprehensive resource hubs
- Establish thought leadership content

## Ongoing Monitoring

Set up recurring visibility tracking:

```
# Schedule weekly visibility check
superlines.create_alert({
  type: "visibility_change",
  threshold: -10,  # Alert if visibility drops 10%+
  queries: ["primary query 1", "primary query 2"],
  notification: "email"
})
```

**Recommended cadence:**
| Check | Frequency |
|-------|-----------|
| Visibility metrics | Weekly |
| Citation analysis | Bi-weekly |
| Competitor review | Monthly |
| Full audit | Quarterly |
