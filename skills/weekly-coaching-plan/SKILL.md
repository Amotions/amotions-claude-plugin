---
name: weekly-coaching-plan
description: Turn the user's recent Amotions AI call scores and coaching into a short practice plan. Use when the user asks how they are doing, whether they are improving, what to work on this week, for a weekly review or one-on-one prep, or for a summary of their recent calls.
---

# Weekly coaching plan

1. Call `get_coaching_trends` twice: `days: 7` for this week and `days: 30` for the baseline. If this week has no calls, use the last 30 days and say so.
2. Call `list_recent_calls` (`days: 7`, `limit: 20`) and pick the highest-scoring and lowest-scoring completed calls. Call `get_call_coaching` for each of those two.
3. Write the plan:
   - **How the week went**: number of calls, average score against the 30-day average, and the outcome counts. One sentence on the direction, without exaggerating a change of a few points.
   - **What worked**: one strength from the best call, with the specific moment if the coaching names it.
   - **Focus for next week**: one skill only, chosen from the most frequent coaching opportunity. Say why it matters for deals, what good looks like, and one line the rep can try on their next call.
   - **Practice**: two short drills, for example a 5-minute role-play you can run with them now, or a question to ask on every call this week.
   - **Calls to revisit**: the lowest-scoring call with its report link, and what to listen for.
4. Keep it under 300 words and talk to the rep directly.

Scores are 0 to 100 from Amotions' post-call analysis. Don't compare the user with teammates; you can only see their own calls. If the user is a manager asking about their team, explain that this plugin only reads the signed-in user's own calls and team reports are in the Amotions web app.

If the Amotions tools are not available, tell the user to connect Amotions AI from this plugin's Connectors tab (the free Amotions plan works).
