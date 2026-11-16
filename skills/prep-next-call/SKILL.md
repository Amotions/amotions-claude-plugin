---
name: prep-next-call
description: Prepare for an upcoming sales call from the user's Amotions AI call history. Use when the user says they have a call, meeting, demo or follow-up coming up, asks to prep or get ready for a call, or asks what to focus on in their next conversation with a prospect or customer.
---

# Prep for the next call

Build a short pre-call brief from the user's own Amotions calls.

1. Find the context.
   - If the user named a prospect, company or earlier call, call `list_recent_calls` (`days: 90`, `limit: 25`) and pick the calls that match. Ask which call if more than one fits; never guess between two people.
   - If this is a first call with someone new, skip to step 3 and use only the user's own patterns.
2. For each matching call (at most 3, newest first), call `get_call_coaching`. Call `get_call_transcript` (`maxChars: 20000`) only for the most recent matching call, to recover what the prospect actually said: their goals, objections, numbers, names, timelines and any promised next step.
3. Call `get_coaching_trends` (`days: 30`) to see what this rep most often needs to work on.
4. Write the brief:
   - **Where it stands**: one or two sentences on the last conversation and the agreed next step, quoting the prospect where it helps.
   - **Their open questions and objections**: bullet list, each with a one-line answer the rep can say out loud.
   - **Goal for this call**: one concrete outcome (for example a booked demo, a decision date, the next stakeholder).
   - **Watch for**: the one or two coaching opportunities from the trends that are most likely to matter on this call, phrased as something to do, not something to avoid.
   - **Opening line**: one natural opener that picks up from the last call.

Keep the brief under 250 words. Use the prospect's words, not invented details. If a transcript or coaching is missing because analysis is still running, say so and work from what is available.

If the Amotions tools are not available, tell the user to connect Amotions AI from this plugin's Connectors tab (the free Amotions plan works) and that you can still help them prep from details they paste in.
