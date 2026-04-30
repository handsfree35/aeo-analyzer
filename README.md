![SEO & AEO Analyzer](aeo.png)

# AEO Analyzer — AI Search Readiness Audit Tool

A working Next.js prototype that analyzes websites for AI-search readiness.

AEO Analyzer checks whether a website is structured in a way that makes it easier for AI answer engines such as ChatGPT, Perplexity and Google AI Overviews to understand, extract and cite the content.

The tool was originally built as a case assignment for a marketing agency to demonstrate how AI-driven audits can become a practical client-facing service.

---

## What It Does

AEO Analyzer takes a URL, fetches the page, analyzes its structure and returns a practical audit report with:

- Overall AEO score
- Short summary of the page’s AI-search readiness
- Prioritized improvement actions
- Detected problems and missing elements
- Positive signals already implemented
- Concrete recommendations for better structure and clarity

---

## Problem

Traditional SEO focuses heavily on search rankings, keywords and backlinks.

AI answer engines work differently. They need content that is easy to parse, summarize and trust. Pages with unclear headings, missing schema, weak FAQ sections, poor answer structure or low trust signals are harder for AI systems to extract reliable answers from.

AEO Analyzer was built to make this problem visible and actionable.

Instead of giving vague advice like “improve your content”, the tool identifies concrete structural issues and turns them into prioritized tasks.

---

## Core Checks

The analyzer looks for signals such as:

- Heading hierarchy
- Question-based H2/H3 structure
- FAQ sections
- FAQPage schema
- Organization schema
- Article / BlogPosting schema
- Product / Service schema where relevant
- Meta title and description quality
- Clear answer sections
- Trust signals
- Author or publisher information
- Review/testimonial signals
- List and table structure
- Semantic clarity for AI extraction

---

## Example Output

The tool returns grouped results such as:

- **Prioritized Actions** — what should be fixed first
- **Problems and Missing Elements** — critical or weak areas
- **What Works Well** — positive signals already present

Example audit categories:

- JSON-LD schema
- H1/H2/H3 structure
- FAQ content
- Clear answer sections
- Meta title and description
- Trust signals
- Content structure

---

## Tech Stack

- **Framework:** Next.js 15
- **Frontend:** React / TypeScript
- **API:** Next.js API route
- **HTML fetching:** Axios
- **HTML parsing:** Cheerio
- **AI analysis:** Claude API
- **Styling:** Tailwind CSS
- **Runtime:** Node.js

---

## Architecture

    User enters URL
        ↓
    Next.js frontend
        ↓
    /api/analyze route
        ↓
    Fetch target HTML with Axios
        ↓
    Parse DOM with Cheerio
        ↓
    Extract structural signals
        ↓
    Send structured context to Claude API
        ↓
    Generate score, findings and recommendations
        ↓
    Render audit report in UI

---

## Why This Matters

AEO, or Answer Engine Optimization, is about making content easier for AI systems to understand and reuse in generated answers.

For marketing agencies, SEO consultants and e-commerce teams, this creates a practical opportunity:

- Audit client websites
- Identify missing structured data
- Improve content for AI answer visibility
- Turn vague AI-search advice into concrete tasks
- Create before/after reports for clients

This prototype demonstrates how that workflow could be productized into a lightweight audit tool.

---

## Screenshots

Add screenshots to a `/screenshots` folder and reference them here:

    screenshots/aeo-analyzer-home.png
    screenshots/aeo-analyzer-result.png

Example:

    ![AEO Analyzer result](screenshots/aeo-analyzer-result.png)

---

## Limitations

This is a working prototype and heuristic audit tool, not a definitive SEO or ranking system.

The analyzer is best suited for:

- Marketing websites
- Service pages
- E-commerce category/product pages
- Blog or article pages
- Agency/client audits

It is less suitable for highly dynamic application interfaces where most value exists behind login, inside dashboards or in client-side app state.

The score should be treated as a directional indicator, not an absolute truth.

---

## Local Setup

Install dependencies:

    npm install

Create an environment file:

    .env.local

Add your Claude API key:

    ANTHROPIC_API_KEY=your_api_key_here

Run the development server:

    npm run dev

Open:

    http://localhost:3000

---

## Environment Variables

Required:

    ANTHROPIC_API_KEY=your_api_key_here

Important:

Do not commit `.env.local` or real API keys to GitHub.

---

## Status

Working prototype.

Built to demonstrate:

- AI-assisted website auditing
- Structured content analysis
- AEO/SEO signal extraction
- Practical agency/client reporting
- Rapid product prototyping with Next.js and Claude API

---

## Possible Next Steps

- Export reports to PDF
- Store audit history per domain
- Add before/after comparison
- Add crawl support for multiple pages
- Add competitor comparison
- Add Open Graph and social metadata checks
- Add Lighthouse/Core Web Vitals integration
- Add agency white-label report mode
- Add authentication and saved projects

---

## Related Work

This project is part of a broader portfolio of backend, automation and e-commerce tools:

- **NordicBeuty** — skincare discovery and price comparison platform
- **Lex Crawler** — async product and price crawler for e-commerce data
- **SentryShield** — lightweight WAF/reverse proxy with bot protection
