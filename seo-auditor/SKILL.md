---
name: seo-auditor
description: A comprehensive SEO audit framework and checklist for web projects. Includes a reusable checklist template, detailed standards, and common validation rules.
---

# SEO Auditor

A battle-tested SEO audit framework extracted from real-world high-traffic projects. Use this to systematically review any new website or page for SEO compliance.

## Resources Included

1.  **[resources/seo_standards.md](resources/seo_standards.md)**: **The Core Knowledge Base**. Detailed guidelines on Metadata, Schema, Content, and Performance standards.
2.  **[resources/checklist_template.md](resources/checklist_template.md)**: A generalized Markdown checklist for auditing any page.
3.  **[resources/audit_rules.js](resources/audit_rules.js)**: A simple Node.js script to check common SEO issues (H1, Meta Tags, Canonical).

## Usage

### 1. Manual Audit (The Golden Standard)
For every significant page update or new feature:

1.  **Read the Standards**: Review `resources/seo_standards.md` to understand the *Why* and *How*.
2.  **Create a Checklist**: Copy `resources/checklist_template.md` to your project (e.g., `docs/audits/PAGE_NAME_AUDIT.md`).
3.  **Verify & Check**: Go through each item. Do not just tick the box—verify it against the standards.

### 2. Automated Check (Sanity Check)
Run the `audit_rules.js` script against your built HTML files to catch obvious errors:

```bash
# Example
node .agent/skills/seo-auditor/resources/audit_rules.js ./out/index.html
```

## Quick Reference (Top 5 Rules)

1.  **Title**: 50-60 chars, unique, dynamic date (e.g. "(June 2026)").
2.  **Canonical**: ALWAYS set, ALWAYS use trailing slash (`/path/`).
3.  **Schema**: Use `FAQPage` (5+ Qs) or `HowTo` to capture rich results.
4.  **Internal Links**: Every page needs 3-6 outgoing links in a "Related" section.
5.  **Performance**: HTML size < 150KB, use `<Image>` component.


## 消费级工具站增量项（evo 实测增补 2026-09-07）

- 动态时间标记 title（Last updated 可见性）——AI 引用偏好的新鲜度信号。
- FAQ accordion 落地（FAQPage schema 与页面可见文本一致，不可只注 schema）。
- HTML 体积 <150KB（首屏效率影响体验分与爬虫预算）。
- 与通用站点框架互查时，以上三项为工具站特有增量；框架通用项照旧。
