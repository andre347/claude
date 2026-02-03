# PostHog Pricing Reference Guide
*Last Updated: June 2025*

## Plan Overview

| Plan | Starting Price | Key Features |
|------|---------------|--------------|
| **Free** | $0/month | 1M events, 5k recordings, 1M feature flag requests, community support, 1 project, 1-year retention |
| **Paid** | Usage-based | Same free limits + overage charges, email support, 6 projects, 7-year retention |
| **Enterprise** | $2,000+/month | SAML SSO, Custom MSA, Dedicated support, Advanced permissions, Audit logs, Unlimited projects |

---

## Core Product Pricing (After Free Tier)

### 🔢 Product Analytics - Events
**Free Tier:** First 1,000,000 events/month

| Volume Range | Anonymous Events | Identified Events |
|--------------|------------------|-------------------|
| 1-2M | $0.00005/event | $0.000248/event |
| 2-15M | $0.0000343/event | - |
| 15-50M | $0.0000295/event | - |
| 50-100M | $0.0000218/event | - |
| 100-250M | $0.000015/event | - |
| 250M+ | $0.000009/event | - |

### 📹 Session Replay
**Free Tier:** First 5,000 recordings/month

| Volume Range | Price per Recording |
|--------------|-------------------|
| 5-15k | $0.005 |
| 15-50k | $0.0035 |
| 50-150k | $0.002 |
| 150-500k | $0.0017 |
| 500k+ | $0.0015 |

### 🚩 Feature Flags
**Free Tier:** First 1,000,000 requests/month

| Volume Range | Price per Request |
|--------------|-------------------|
| 1-2M | $0.0001 |
| 2-10M | $0.000045 |
| 10-50M | $0.000025 |
| 50M+ | $0.00001 |

### 🧪 Experiments (A/B Testing)
**Free Tier:** First 1,000,000 requests/month

| Volume Range | Price per Request |
|--------------|-------------------|
| 1-2M | $0.0001 |
| 2-10M | $0.000045 |
| 10-50M | $0.000025 |
| 50M+ | $0.00001 |

### 📊 Surveys
**Free Tier:** First 250 responses/month

| Volume Range | Price per Response |
|--------------|-------------------|
| 250-500 | $0.20 |
| 500-1k | $0.10 |
| 1-10k | $0.035 |
| 10-20k | $0.015 |
| 20k+ | $0.01 |

### 🔄 Data Pipelines
**Free Tier:** First 1,000,000 rows/month

| Volume Range | Price per Row |
|--------------|---------------|
| 1-10M | $0.000015 |
| 10-100M | $0.00001 |
| 100M+ | $0.000008 |

### ⚡ Web Performance
**Free Tier:** First 100,000 exceptions/month

| Volume Range | Price per Exception |
|--------------|-------------------|
| 100-325k | $0.00037 |
| 325k-10M | $0.00014 |
| 10M+ | $0.000115 |

---

## Add-On Products

### 🔄 Event-Based Add-ons (Applied to Total Product Analytics Volume)
*These charges are calculated using your total Product Analytics event volume*

| Add-On | Price per Event | Free Tier | Notes |
|--------|-----------------|-----------|-------|
| **Identified Events** | $0.000198/event | 1M/month | Enhanced user tracking with person profiles |
| **Group Analytics** | $0.000071/event | 1M/month | B2B analytics - track company/organization events |
| **Data Pipelines** | $0.000062/event | 1M/month | Export to BigQuery, Redshift, Customer.io, etc. |

### 📦 Fixed-Price Add-ons

| Add-On | Price | Free Tier | Notes |
|--------|-------|-----------|-------|
| **Teams** | $450/month | N/A | Priority support, unlimited projects, white labeling, HIPAA BAA, SSO enforcement |
| **Mobile Session Replay** | $0.01/recording | 2.5k/month | iOS and Android session recordings |

---

## Annual Plans & Discounts

### Credit Purchase Discounts
| Annual Credit Purchase | Discount |
|----------------------|----------|
| $6,000 - $20,000 | 10% |
| $20,000 - $50,000 | 15% |
| $50,000 - $100,000 | 20% |
| $100,000+ | 25% |

### Other Discounts
- **Non-profits:** 25% discount (email sales@posthog.com)
- **Startups:** 25% discount (subject to approval)
- **Volume commitments:** Custom pricing available

---

## Key Pricing Notes for Account Management

### 💡 **Upsell Opportunities**
1. **Product Expansion:** Look for single-product users who could benefit from the integrated suite
2. **Volume Growth:** Accounts approaching free tier limits
3. **Annual Commitments:** Monthly payers who could save 10-25% with annual plans
4. **Add-on Features:** Teams add-on for larger organizations, Group Analytics for B2B companies

### ⚠️ **Important Considerations**
- **No Renewal Dates for Monthly Plans:** Only annual plan customers have true "renewal dates"
- **Free Tier Resets Monthly:** Generous limits mean 90%+ of users stay free
- **Usage-Based Scaling:** Costs decrease significantly with volume
- **Enterprise Threshold:** $2,000/month minimum for enterprise features

### 📈 **Revenue Calculation Tips**
- **MRR Estimation:** Use previous 3 months average usage × pricing tiers
- **Growth Projection:** Factor in typical 20-30% monthly growth for growing companies
- **Multi-Product Value:** Integrated suite typically 40-60% cheaper than point solutions

### 🧮 **Add-on Revenue Calculation Example**
For an account with **5M total Product Analytics events/month** using Identified Events and Group Analytics:

**Base Product Analytics Cost:**
- First 1M events: Free
- 1-2M events: 1M × $0.00005 = $50
- 2-15M events: 3M × $0.0000343 = $102.90
- **Total Base Cost: $152.90**

**Add-on Costs (applied to full 5M volume):**
- Identified Events: (5M - 1M free) × $0.000198 = $792
- Group Analytics: (5M - 1M free) × $0.000071 = $284
- **Total Add-on Cost: $1,076**

**Total Monthly Cost: $152.90 + $1,076 = $1,228.90**

### 🎯 **Expansion Targeting**
- **High Event Volume, No Add-ons:** Prime targets for Identified Events/Group Analytics (can dramatically increase MRR)
- **Single Product Users:** Suite expansion opportunities
- **Approaching Free Limits:** Ready for paid conversion
- **Manual Data Processes:** Good candidates for Data Pipelines add-on
- **Growing Teams:** Teams add-on opportunity ($450/month flat fee)
- **B2B Companies:** Group Analytics is essential for company-level insights

---

## Vitally Data Mapping for Revenue Calculations

### 📊 **Key Metrics to Pull from Vitally:**
- **Product Analytics Events:** Use for base pricing + all event-based add-ons
- **Session Recordings:** Separate pricing tier
- **Feature Flag Requests:** Separate pricing tier  
- **A/B Test Requests:** Separate pricing tier
- **Survey Responses:** Separate pricing tier
- **Data Pipeline Rows:** Separate pricing tier
- **Web Performance Exceptions:** Separate pricing tier

### 💰 **Revenue Stream Priority:**
1. **Event-based add-ons** (highest revenue potential per customer)
2. **Teams add-on** ($450/month flat - easy wins for larger orgs)
3. **Annual plan conversions** (10-25% discount = immediate revenue boost)
4. **New product adoption** (Session Replay, Feature Flags, etc.)

---

## Quick Reference: Most Common Pricing Scenarios

| Scenario | Monthly Volume | Estimated Monthly Cost |
|----------|----------------|----------------------|
| **Small SaaS** | 500k events, 2k recordings | ~$50-100 |
| **Growing Startup** | 5M events, 20k recordings | ~$300-500 |
| **Mid-Market** | 25M events, 100k recordings | ~$1,500-2,500 |
| **Enterprise** | 100M+ events, 500k+ recordings | $5,000+ |

*Note: All prices in USD, excluding taxes. Volume discounts apply at scale.*