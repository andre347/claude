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

## Slack Message when starting a new channel with customer and inviting them

Hey @_name_ got this channel set up for easier coordination with the team. Anyone else may be good to bring in here? I'm unsure who's managing the posthog instance from your side most recently. And on top of that your spend has been ramping up, so i want to make sure I can help with any optimization or other tips if needed!

totally fine if you wanna keep things async, but generally it's useful for both sides to get on a live call to help me understand your current posthog setup so i can best help you, talk roadmap or feedback, or discounting. I'm a combo-engineer+account manager for you all in one. Can we get a time set-up this week? 30 Min Cal
