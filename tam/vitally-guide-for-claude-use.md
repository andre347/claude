# Vitally Account Management Process Guide

## Account Search Process

### 1. ALWAYS Start with Cached Account Search

```
Step 1: Search cached accounts first using vitally:search_accounts_advanced
- Filter by csmEmail: "andre@posthog.com" to get current account list
- ALWAYS report: "Using cached data - last refresh: [timestamp from response]"
- If cache is stale (>24 hours), offer to refresh
```

### 2. Account Search Hierarchy

**Primary Method:** Use andre's account list from knowledge base

- Match account name from user request to account list
- Extract the External ID (e.g., "018618b5-1d96-0000-227e-a5b4f568d00b")
- Use External ID in vitally:get_account_full for complete details

**Backup Methods (if name not in list):**

1. `vitally:find_account_by_name` - for partial matches
2. `vitally:search_accounts` - basic name search
3. `vitally:search_accounts_advanced` - with filters if needed

### 3. Account Refresh Process

- Use `vitally:refresh_accounts` only when:
  - Cache is >24 hours old
  - User specifically requests fresh data
  - Account not found in current cache

## Note Creation Process

### Correct Note Structure:

**Subject:** Brief purpose (e.g., "account check", "usage review") - goes in separate `subject` parameter

**Content:** Rich text body (NOT markdown), following template:

```
Key Findings (Max 8 bullets):
• [Product usage highlight]
• [Billing/revenue action]
• [Technical implementation]
• [Critical action item] (use bold rich text formatting)
```

### Format Requirements:

- **Content:** Rich text formatting (bold, bullets, etc.)
- **Subject:** Plain text, concise purpose statement
- **NO Markdown:** Use rich text formatting instead

### Rich Text Formatting Examples:

- **Bold text:** `<strong>Critical action item</strong>`
- **Bullets:** `<ul><li>Product usage highlight</li><li>Billing action needed</li></ul>`
- **Emphasis:** `<em>italics</em>` or `<strong>bold</strong>`
- **Line breaks:** `<br>` for single line breaks
- **Paragraphs:** `<p>Content here</p>`

### HTML Note Content Example:

```html
<p><strong>Key Findings:</strong></p>
<ul>
  <li>MRR increased 15% to $3,200</li>
  <li>Set session replay billing limit to $1,500</li>
  <li>Using 3 of 6 available products</li>
  <li><strong>SDK versions 6 months outdated</strong></li>
  <li>Strong adoption of feature flags (80% of users)</li>
  <li>2 open support tickets, both low priority</li>
  <li>No annual contract discussions yet</li>
  <li>Expansion opportunity: surveys product</li>
</ul>
```

## Task Creation Process

### Tool Parameters:

```
vitally:create_account_task requires:
- accountId (required)
- title (required) ✅ This works correctly
- description (optional)
- dueDate (optional, ISO format)
- priority (optional: low/medium/high/urgent)
```

### Best Practices:

- **Title:** Concise, actionable (e.g., "Schedule Q4 renewal call")
- **Description:** Context and specific steps needed
- **Priority:** Use "high" for revenue-critical items
- **Due Date:** Always include for accountability

## Revenue Threshold Guidelines

### Product Adoption Criteria:

- **Trivial/Experimental:** <$100 monthly spend
- **Adopted:** $100+ monthly spend
- **Significant:** $500+ monthly spend

### Focus Areas:

- Accounts <$20k ARR need attention
- Monthly billing customers → convert to annual
- Single-product users → cross-sell opportunities
- High event volume without add-ons → upsell targets

## Error Handling

### If Account Not Found:

1. Check andre's account list spelling
2. Try partial name search
3. Search by external ID if available
4. Refresh cache if needed
5. Report: "Account not found in current cache or may not be assigned to andre"

### If API Errors:

1. Report specific error message
2. Suggest alternative approach
3. Note confidence level in recommendations

---
