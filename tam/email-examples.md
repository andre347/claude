# Rolling off the startup plan

engineer from PostHog's account team here - giving a quick heads up that you're rolling off the startup plan next month (so covered for the xx bill, but the xxx bill will be your first paid month).

You guys have ramped up quite a bit, congrats on the growth. Does your current spend level make sense for you to pay when you roll off at the end of March? Currently $x/mo - you can view usage/breakdown at us.posthog.com/organization/billing.

Happy to help you trim down cost - biggest lever here is going to be getting rid of $autocapture and $screen events (or limiting them), since you already have a bunch of custom events instrumented.

There are other ways to save you $ as well (all of them involve buying credits upfront for a discount). Grab time in my signature if you want to chat through any of this.

## Email for error tracking

Hey X, X from PostHog here.

Your bill shot up again last month, and given the previous refund we gave, I wanted to ensure that all is ok on your end?

I noticed one of your events query:error from the web library, and it made me think it might be better to capture these errors as exceptions and use our Error Tracking product? Looks like the cost would be similar or less for the errors given the free tier, plus you would get

- Automatic issue grouping – similar errors are grouped together by type, message, and stack trace
- Rich debug data – stack traces, exception type, severity level, and fingerprints captured automatically
- Source map support – minified code is resolved to readable stack traces
- The error tracking UI – triage, assign, and resolve issues in /error_tracking
- No trade-offs – exception events still work in insights, session replay filters, surveys, etc.

Thought it might be worth mentioning. Feel free to tell me I am stupid and theres a better reason to keep it as an event!

Best
