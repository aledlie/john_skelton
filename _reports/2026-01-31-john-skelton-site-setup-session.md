---
layout: single
title: "John Skelton Site Setup: Domain, GitHub Pages, and Compliance Documentation"
date: 2026-01-31
author_profile: true
categories: [infrastructure, documentation]
tags: [github-pages, porkbun-api, doppler, jekyll, regulatory-compliance, domain-registration]
excerpt: "Complete site infrastructure setup including domain availability checks via Porkbun API, GitHub repository creation, Pages configuration, and regulatory link enhancement for compliance documentation."
header:
  image: /assets/images/cover-reports.png
  teaser: /assets/images/cover-reports.png
---

# John Skelton Site Setup: Domain, GitHub Pages, and Compliance Documentation

**Session Date**: 2026-01-31<br>
**Project**: john_skelton (Personal Site)<br>
**Focus**: Infrastructure setup and documentation enhancement<br>
**Session Type**: Implementation

---

## Executive Summary

This session established the complete infrastructure for John Skelton's personal site, from domain research through GitHub Pages deployment. Using Doppler-authenticated Porkbun API calls, we verified domain availability across 9 TLD variations, identifying `johnskelton.blog` as available at $3.60/year promotional pricing.

The session also enhanced the Leora Home Health compliance analysis document with 17 regulatory links, fixing 2 broken URLs and adding inline hyperlinks to authoritative government sources (EEOC, FLSA, CMS, HIPAA, OIG, SAM, Joint Commission, TWC, IRS).

## Key Metrics

| Metric | Value |
|--------|-------|
| Domains checked | 9 |
| Available domains found | 5 |
| Regulatory links added/fixed | 17 |
| Broken URLs corrected | 2 |
| GitHub commits | 2 |
| Files modified | 2 |

---

## 1. Compliance Document Enhancement

### Link Audit Results

Audited `_work/leora-policy-compliance-summary.md` for missing regulatory links using the content-creator skill.

**URLs Verified via Playwright MCP:**
- `https://www.dol.gov/agencies/whd/flsa` - Valid
- `https://exclusions.oig.hhs.gov/` - Valid
- `https://sam.gov/` - Valid
- `https://www.jointcommission.org/` - Valid
- `https://tlc.texas.gov/` - Valid
- `https://www.irs.gov/forms-pubs/about-form-w-2` - Valid
- `https://www.eeoc.gov/guidance` - Valid (fixed from `/laws/guidance`)
- `https://www.twc.texas.gov/jobseekers/employee-rights-laws` - Valid (fixed from `/businesses/employment-law`)

**Broken URLs Fixed:**
1. EEOC: `/laws/guidance` → `/guidance`
2. TWC: `/businesses/employment-law` → `/jobseekers/employee-rights-laws`

**Inline Links Added:**
- Line 29: EEOC, FLSA in Key Compliance Areas
- Line 65: EEOC section header
- Line 80: FLSA section header
- Line 84: W-2 reference
- Line 95: Texas Legislative Council
- Line 123: OIG, SAM exclusion databases
- Line 133: CMS section header
- Line 186: HIPAA section header
- Line 308: Joint Commission
- Line 350: Texas Legislative Council (author bio)

**Related Resources Section Expanded:**
Added 7 new authoritative links including DOL FLSA, OIG Exclusions Database, SAM.gov, and Joint Commission.

---

## 2. Domain Availability Research

### Porkbun API Integration

Used Doppler secrets management with `integrity-studio` project for authenticated API calls.

```bash
doppler run --project integrity-studio --config dev -- bash -c \
  'curl -s -X POST "https://api.porkbun.com/api/json/v3/domain/checkDomain/$domain" \
  -H "Content-Type: application/json" \
  -H "User-Agent: Mozilla/5.0" \
  -d "{\"apikey\": \"$PORKBUN_API_KEY\", \"secretapikey\": \"$PORKBUN_SECRET_API_KEY\"}"'
```

### Domain Check Results

| Domain | Available | Price/yr |
|--------|-----------|----------|
| johnskelton.com | No | $11.08 |
| jskelton.com | No | $11.08 |
| john-skelton.com | No | $11.08 |
| johnskelton.dev | **Yes** | $10.81 |
| johnskelton.io | **Yes** | $28.12 |
| johnskelton.net | **Yes** | $12.52 |
| johnskelton.blog | **Yes** | $3.60 (promo) |
| jskelton.dev | **Yes** | $10.81 |
| jskelton.net | No | $12.52 |
| skelton.com | No | $11.08 |
| skelton.dev | No | $10.81 |

**Selected Domain**: `johnskelton.blog` - $3.60 first year, $21.11 renewal

### Registration Attempt

```json
{"status":"ERROR","message":"No funds."}
```

User completed registration manually via Porkbun web interface.

---

## 3. GitHub Repository Setup

### Repository Creation

```bash
gh repo create john_skelton --public --source=. --push
```

**Repository URL**: https://github.com/aledlie/john_skelton

### Commits

1. `7842ce9` - docs(work): add regulatory links and enhance Leora compliance summary
2. `2c84980` - chore: add CNAME for johnskelton.blog custom domain

---

## 4. GitHub Pages Configuration

### CNAME Setup

```bash
echo "johnskelton.blog" > CNAME
git add CNAME && git commit && git push
```

### Pages API Configuration

```bash
gh api repos/aledlie/john_skelton/pages -X POST \
  --input - <<< '{"source":{"branch":"main","path":"/"}}'
```

**Response:**
```json
{
  "url": "https://api.github.com/repos/aledlie/john_skelton/pages",
  "cname": "johnskelton.blog",
  "html_url": "http://johnskelton.blog/",
  "source": {"branch": "main", "path": "/"},
  "public": true
}
```

HTTPS certificate issuance initiated (typically 10-15 minutes).

---

## 5. Local Development Verification

### Jekyll Server Status

```bash
lsof -i :4000
# COMMAND   PID          USER   FD   TYPE  NODE NAME
# ruby    70177 alyshialedlie    6u  IPv4  TCP localhost:terabase (LISTEN)
```

Site confirmed running at `http://localhost:4000` with Minimal Mistakes theme.

---

## Files Modified

| File | Changes |
|------|---------|
| `_work/leora-policy-compliance-summary.md` | +30/-13 lines (17 links added) |
| `CNAME` | Created (1 line) |

---

## Tools & Integrations Used

- **Doppler**: Secrets management for Porkbun API credentials
- **Porkbun API**: Domain availability checks and registration
- **GitHub CLI (gh)**: Repository creation, Pages configuration
- **Playwright MCP**: URL verification via webresearch tools
- **Jekyll**: Local development server

---

## Next Steps

1. Verify HTTPS certificate issuance at GitHub Pages settings
2. Enable "Enforce HTTPS" once certificate is ready
3. Configure DNS if not auto-configured by Porkbun
4. Review site at https://johnskelton.blog once propagation complete

---

## References

- Repository: https://github.com/aledlie/john_skelton
- Live Site: https://johnskelton.blog
- Porkbun API Docs: https://porkbun.com/api/json/v3/documentation
- GitHub Pages Docs: https://docs.github.com/en/pages
