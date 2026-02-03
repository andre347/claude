## How to Use This Framework

When conducting account research, systematically review each account against these criteria using available Vitally data. Look for patterns in usage metrics, billing data, and engagement indicators to identify actionable insights.

---

## Opportunities

### Revenue Expansion
1. **MoM event growth** - Look for sustained month-over-month increases in event volume
   - Check: `event_count_in_month` vs previous periods, `diff_dollars` positive, `forecasted_mrr` > `mrr`
   - **Value**: Projected MRR increase based on growth trajectory (e.g., 20% growth = 0.2 × current MRR)
   - **Confidence**: 60-75% (depends on growth consistency and trends)

2. **New users being invited** - Increasing user count indicates organizational expansion
   - Check: `usersCount` trending up, `user_count` growth patterns
   - **Value**: $50-200 ARR per new user (based on average revenue per user)
   - **Confidence**: 50-70% (user growth doesn't always correlate with revenue)

3. **Frequent logins and active usage** - High engagement rates show strong product-market fit
   - Check: `lastSeenTimestamp` recent, `vitally.custom.ofActiveUsersAnalyzingInsightsAndDashboardsLast14Days` >50%
   - **Value**: Expansion readiness indicator - estimate 15-30% MRR uplift potential
   - **Confidence**: 40-60% (engagement indicates expansion readiness but timing varies)

4. **Adding new addons, or paid products** - Recent product expansion shows willingness to invest
   - Check: `vitally.custom.totalProductsPaid` increasing, new items in `vitally.custom.paidProducts`
   - **Value**: Historical expansion momentum - estimate 20-40% additional expansion in next 6 months
   - **Confidence**: 65-80% (recent expansion predicts future expansion)

5. **Crossing 60k ARR** - Eligible for higher volume discounts and enterprise features
   - Check: `mrr` * 12 approaching or exceeding $60,000
   - **Value**: Enterprise upsell opportunity - typically 25-50% MRR increase
   - **Confidence**: 70-85% (clear pricing tier transition)

6. **MRR increase by x percent** - Significant revenue growth indicates expansion opportunity
   - Check: `forecasted_mrr` vs `mrr` percentage increase, `diff_dollars` positive trends
   - **Value**: Direct calculation from forecasted_mrr - mrr
   - **Confidence**: 85-95% (based on actual usage projections)

7. **Monthly customers eligible for annual plan conversion** - 10-25% savings opportunity
   - Check: Missing "Annual Plan" in `segments`, `stripe.subscriptionInterval` = "month", MRR >$500
   - **Value**: 12 × current MRR (annual commitment)
   - **Confidence**: 90-95% (fixed pricing conversion)

8. **High usage approaching billing limits** - Natural upsell moment when limits are hit
   - Check: `*_billing_limit` fields vs actual usage metrics, usage at 80%+ of limits
   - **Value**: Estimate increased usage tier costs (typically 30-100% MRR increase)
   - **Confidence**: 80-90% (usage trajectory is predictable)

9. **Single-product users** - Cross-sell session replay, feature flags, surveys, etc.
   - Check: `vitally.custom.totalPaidProductCountMainOnly` = 1, specific products missing from `vitally.custom.paidProducts`
   - **Value**: $200-2000 ARR per additional product (based on typical product MRR)
   - **Confidence**: 60-75% (varies by product fit and use case)

10. **Teams add-on opportunity** - Organizations >50 people without Teams plan ($450/month)
    - Check: `sfdc.NumberOfEmployees` >50, missing "Teams Plan" in `segments`, no `teams_plan`
    - **Value**: $5,400 ARR (fixed pricing)
    - **Confidence**: 95% (clear pricing, obvious fit criteria)

11. **B2B business but not using group analytics** - Essential for company-level insights
    - Check: `sfdc.Company_Type__c` = "private", `group_types_total` = 0, no `group_analytics_plan`
    - **Value**: $500-5000 ARR (based on event volume × group analytics pricing)
    - **Confidence**: 75-85% (clear B2B need, usage-based pricing)

12. **High event volume without identified events add-on** - High-value revenue expansion
    - Check: High `event_count_in_month`, `vitally.custom.enhancedPersonsPaid` = 0 or null
    - **Value**: Event volume × $0.000198 = potential identified events ARR
    - **Confidence**: 80-90% (clear usage-based calculation)

13. **Strong data pipeline usage growth** - Shows data maturity and expansion potential
    - Check: `vitally.custom.rowsSyncedLast30DaysIfSendingData` >1M, `active_batch_exports` >0
    - **Value**: Rows synced × $0.000015 = potential pipeline ARR expansion
    - **Confidence**: 70-85% (usage-based pricing with clear metrics)

14. **Multiple external data schemas added** - Data warehouse upsell opportunity
    - Check: `active_external_data_schemas` >5, no `data_warehouse_plan` or low DW usage
    - **Value**: $1,000-10,000 ARR (based on data complexity and query volume)
    - **Confidence**: 60-75% (varies significantly by use case)

### Engagement Signals
15. **High admin user percentage** - Indicates strong organizational buy-in
    - Check: `admin_emails` count vs `usersCount` ratio >20%
    - **Value**: Expansion readiness - estimate 20-40% MRR uplift potential
    - **Confidence**: 50-65% (engagement indicator, not direct revenue driver)

16. **Multiple projects created** - Shows expansion within organization
    - Check: `project_count` >2, multiple active projects
    - **Value**: $1,000-5,000 ARR per additional active project/team
    - **Confidence**: 65-80% (additional projects often mean additional usage)

17. **Strong feature flag adoption rates** - Engineering team actively engaged
    - Check: `vitally.custom.ofActiveUsersCreatingFeatureFlags` >50%, `vitally.custom.featureFlagRequestsLast30DaysIfSendingData` >100K
    - **Value**: Feature flag usage expansion - requests × pricing tiers
    - **Confidence**: 75-85% (usage-based calculation)

18. **Survey responses increasing** - Product team actively collecting feedback
    - Check: `survey_responses_count_in_month` trending up, `vitally.custom.ofActiveUsersUsingSurveysLast14Days` >0
    - **Value**: Survey response volume × $0.20-0.01 (tiered pricing)
    - **Confidence**: 80-90% (direct usage-based pricing)

19. **High session replay analysis rates** - Active usage of premium features
    - Check: `vitally.custom.ofActiveUsersAnalyzingRecordingsLast14Days` >30%, `vitally.custom.replayCountLast30DaysIfSendingData` >10K
    - **Value**: Recording volume × tiered replay pricing
    - **Confidence**: 85-95% (clear usage-based revenue)

20. **Dashboard creation activity** - Shows analytical maturity and value realization
    - Check: `vitally.custom.insightDashboardAnalyzedPerActiveUserLast14Days` >5
    - **Value**: Retention/expansion readiness - estimate 10-25% lower churn risk
    - **Confidence**: 40-60% (engagement indicator, indirect revenue impact)

21. **Integration/webhook usage growing** - Deeper platform integration
    - Check: `active_hog_destinations` >0, `active_hog_transformations_schemas` >0
    - **Value**: Data pipeline expansion potential - estimate $500-3000 ARR
    - **Confidence**: 60-75% (integration depth varies significantly)

### Business Intelligence
22. **Recent funding rounds** - Expansion budget likely available
    - Check: `sfdc.harmonic_last_funding_date__c` within last 12 months, `sfdc.Clearbit_Raised__c` >$1M
    - **Value**: Budget expansion opportunity - estimate 50-200% MRR increase potential
    - **Confidence**: 40-60% (funding doesn't guarantee spending, timing varies)

23. **Headcount growth indicators** - More seats and usage expected
    - Check: `sfdc.harmonic_headcount__c` vs `sfdc.harmonic_headcount_180d__c` positive growth
    - **Value**: Headcount growth % × current MRR (more users = more usage)
    - **Confidence**: 70-85% (headcount growth strongly correlates with usage)

24. **Strong NPS scores** - Account ready for expansion conversations
    - Check: `npsScore` >50, `npsPromoterCount` > `npsDetractorCount`
    - **Value**: Expansion conversation readiness - estimate 25-50% higher close rates
    - **Confidence**: 60-75% (satisfaction enables expansion but timing varies)

25. **Low support ticket volume** - Healthy implementation, ready for growth
    - Check: `vitally.custom.supportTickets` <3, `vitally.custom.numberOfTicketsOpenedLast30Days` = 0
    - **Value**: Expansion readiness indicator - estimate 20-40% higher expansion success
    - **Confidence**: 55-70% (health indicator, indirect revenue impact)

---

## Risks

### Usage Decline
1. **No recent logins or activity** - Critical engagement risk indicator
   - Check: `lastSeenTimestamp` >30 days old, `lastInboundMessageTimestamp` >60 days old
   - **Risk Value**: 70-90% of current ARR at risk within 6 months
   - **Confidence**: 85-95% (strong predictor of churn)

2. **10% decrease in 30 days of events** - Usage pattern decline risk
   - Check: `event_count_in_month` vs previous period, `diff_dollars` negative >10%
   - **Risk Value**: 40-60% of current ARR at risk within 3-6 months
   - **Confidence**: 75-85% (usage decline strongly correlates with churn)

3. **Products being paid for but not used at all** - Immediate churn risk
   - Check: Products in `vitally.custom.paidProducts` but usage metrics = 0 or null for that product
   - **Risk Value**: 100% of unused product MRR immediately, 30-50% total account risk
   - **Confidence**: 90-95% (unused paid products are almost always churned)

4. **Decreasing user count month-over-month** - Organizational disengagement  
   - Check: `usersCount` trending down, `user_count` decline patterns
   - **Risk Value**: User decline % × current ARR (fewer users = less value)
   - **Confidence**: 80-90% (user count decline predicts revenue decline)

5. **Low percentage of active vs. total users** - Poor adoption within organization
   - Check: Active user metrics <30% of `usersCount`, low engagement percentages
   - **Risk Value**: 25-45% of current ARR at risk (low adoption = low stickiness)
   - **Confidence**: 70-80% (adoption rates correlate with retention)

6. **Dashboard/insight creation dropping off** - Declining analytical engagement
   - Check: `vitally.custom.insightDashboardAnalyzedPerActiveUserLast14Days` <1, declining trends
   - **Risk Value**: 20-40% of current ARR at risk (reduced value realization)
   - **Confidence**: 65-75% (analytical engagement indicates value perception)

7. **Session replay recording volume declining** - Premium feature abandonment
   - Check: `vitally.custom.replayCountLast30DaysIfSendingData` declining, `session_replay_ltv` flat
   - **Risk Value**: Session replay MRR at immediate risk, 15-30% total account risk
   - **Confidence**: 80-90% (feature-specific decline is predictive)

8. **Feature flag request volume dropping** - Engineering team disengagement
   - Check: `vitally.custom.featureFlagRequestsLast30DaysIfSendingData` declining >20%
   - **Risk Value**: Feature flag MRR at risk, 20-35% total account risk
   - **Confidence**: 75-85% (engineering team disengagement is critical)

9. **Long periods between logins by key users** - Champion disengagement risk
   - Check: Key admin emails in `admin_emails` with low activity indicators
   - **Risk Value**: 40-70% of current ARR at risk (champion loss = high churn risk)
   - **Confidence**: 70-85% (champion engagement is crucial for retention)

10. **Project abandonment** - Multiple projects created but only one active
    - Check: `project_count` >2 but usage concentrated in one project only
    - **Risk Value**: 20-40% of current ARR at risk (reduced organizational footprint)
    - **Confidence**: 60-75% (project consolidation often precedes downsizing)

### Technical/Implementation
11. **Frequent billing limit hits** - Budget constraint indicators
    - Check: Usage at 100% of `*_billing_limit` fields, frequent limit adjustments
    - **Risk Value**: Growth constraint = 50-80% of expansion potential lost, 20-30% churn risk
    - **Confidence**: 80-90% (budget constraints directly impact growth and retention)

12. **Integration failures or webhook errors** - Technical implementation issues
    - Check: `active_hog_destinations` errors, integration health metrics
    - **Risk Value**: 30-50% of current ARR at risk (poor experience drives churn)
    - **Confidence**: 65-80% (technical issues impact value realization)

13. **Data quality issues** - High error rates affecting value realization
    - Check: `error_tracking_ltv` increasing, high exception counts
    - **Risk Value**: 25-45% of current ARR at risk (data quality affects trust)
    - **Confidence**: 70-85% (data quality directly impacts value perception)

14. **Old SDK versions** - Performance/security risks, poor experience
    - Check: SDK version data (if available), implementation quality indicators
    - **Risk Value**: 15-30% of current ARR at risk (poor performance drives dissatisfaction)
    - **Confidence**: 60-75% (technical debt creates friction but timing varies)

15. **Single point of failure** - Only one admin user, organizational risk
    - Check: `admin_emails` count = 1, single user dependency
    - **Risk Value**: 60-90% of current ARR at risk if key person leaves
    - **Confidence**: 70-85% (single points of failure create high vulnerability)

### Business Relationship
16. **Increasing support ticket volume** - Implementation or satisfaction issues
    - Check: `vitally.custom.supportTickets` >5, `vitally.custom.numberOfTicketsOpenedLast30Days` increasing
    - **Risk Value**: 20-40% of current ARR at risk (satisfaction issues drive churn)
    - **Confidence**: 70-80% (support burden correlates with churn likelihood)

17. **Long response times to CSM outreach** - Declining relationship health
    - Check: `lastInboundMessageTimestamp` vs `lastOutboundMessageTimestamp` gaps >14 days
    - **Risk Value**: 30-50% of current ARR at risk (relationship deterioration)
    - **Confidence**: 65-80% (communication breakdown is leading churn indicator)

18. **Open urgent tickets unresolved >7 days** - Critical satisfaction risk
    - Check: `vitally.custom.numberOfUrgentTicketsCreatedInLast30Days` >0, ticket age
    - **Risk Value**: 50-80% of current ARR at risk (urgent issues unresolved)
    - **Confidence**: 85-95% (urgent unresolved issues are strong churn predictors)

19. **Key champion departure** - Relationship continuity risk (if trackable)
    - Check: Changes in `admin_emails`, key contact role changes
    - **Risk Value**: 60-90% of current ARR at risk (champion loss = relationship reset)
    - **Confidence**: 80-90% (champion departures significantly increase churn risk)

20. **No clear use case identification** - Lack of value demonstration
    - Check: Low engagement across all product areas, no dominant use case
    - **Risk Value**: 40-70% of current ARR at risk (unclear value = weak retention)
    - **Confidence**: 70-85% (value clarity is fundamental to retention)

21. **Credit balance running low without payment method** - Payment risk
    - Check: `stripe.accountBalance` approaching zero, `amount_off_expires_at` approaching
    - **Risk Value**: 100% of current ARR at immediate risk (payment failure)
    - **Confidence**: 95-99% (payment method issues directly cause churn)

22. **Failed payment attempts** - Immediate churn risk
    - Check: `stripe.delinquent` = true, payment method issues
    - **Risk Value**: 100% of current ARR at immediate risk
    - **Confidence**: 95-99% (failed payments = immediate churn)

23. **Approaching renewal date with low engagement scores** - Renewal risk
    - Check: `nextRenewalDate` <90 days, `healthScore` <6, low usage metrics
    - **Risk Value**: 70-95% of current ARR at risk (renewal failure likely)
    - **Confidence**: 85-95% (low engagement + renewal proximity = high churn probability)

### Market/Competitive
24. **Similar accounts churning** - Cohort risk patterns
    - Check: Similar `segments`, industry, size accounts with churn patterns
    - **Risk Value**: 30-60% of current ARR at risk (cohort effects)
    - **Confidence**: 50-70% (market patterns affect individual accounts but timing varies)

25. **Usage patterns similar to known churn signals** - Predictive risk indicators
    - Check: Combination of declining metrics matching historical churn patterns
    - **Risk Value**: 50-80% of current ARR at risk (predictive model output)
    - **Confidence**: 75-90% (historical pattern matching is strong predictor)

26. **Trial conversion deadline approaching without positive signals** - Conversion risk
    - Check: `trialEndDate` approaching, `trial_status` = "active", low engagement metrics
    - **Risk Value**: 100% of potential ARR lost (trial won't convert)
    - **Confidence**: 85-95% (trial conversion patterns are highly predictable)

---

## Using Dollar Values & Confidence Scores

### Value Calculation Guidelines

**Opportunity Values:**
- **Fixed pricing items** (Teams add-on, annual plans): Use exact pricing
- **Usage-based estimates**: Apply current usage × pricing tiers  
- **Expansion readiness**: Estimate 15-50% of current MRR as potential uplift
- **Cross-sell potential**: $200-2,000 ARR per additional product

**Risk Values:**
- **Immediate risks** (payment failures): 100% of ARR at risk
- **Strong churn indicators**: 70-95% of ARR at risk
- **Usage decline**: 20-60% of ARR at risk (based on severity)
- **Relationship issues**: 30-70% of ARR at risk

### Confidence Score Interpretation

**90-95% Confidence**: Fixed pricing, clear calculations, immediate payment issues
**75-89% Confidence**: Usage-based calculations with solid data, strong behavioral patterns
**60-74% Confidence**: Trend-based estimates, engagement indicators, market factors
**40-59% Confidence**: Early signals, timing uncertainty, indirect indicators

### Prioritization Framework

**Priority Score = (Dollar Value × Confidence Score) / 100**

**High Priority** (Score >$2,000): Immediate action required
**Medium Priority** (Score $500-2,000): Plan action within 30 days  
**Low Priority** (Score <$500): Monitor and revisit quarterly

### Example Account Assessment Output

**🔴 RISKS IDENTIFIED:**
- Payment failure risk: -$42,000 ARR (95% confidence) = **-$39,900 priority score**
- Usage decline: -$15,000 ARR (80% confidence) = **-$12,000 priority score**
- **Total Risk: -$46,900 priority score**

**🟢 OPPORTUNITIES IDENTIFIED:**
- Teams add-on: +$5,400 ARR (95% confidence) = **+$5,130 priority score**
- Group analytics upsell: +$3,200 ARR (80% confidence) = **+$2,560 priority score**
- **Total Opportunity: +$7,690 priority score**

**📊 ACCOUNT PRIORITY: HIGH RISK** (Net: -$39,210 priority score)
**Recommended Action**: Immediate retention intervention required

---

*Last Updated: July 24, 2025*