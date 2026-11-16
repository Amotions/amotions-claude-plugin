---
name: handle-objections
description: Review how the user handled objections on their Amotions AI sales calls and give better responses to practice. Use when the user asks what objections came up, how they could have answered better, why a deal stalled, or wants to practice price, timing, competitor, trust or "send me info" pushback.
---

# Review and sharpen objection handling

1. Pick the calls.
   - One call: if the user named it, use it; otherwise use the most recent completed call from `list_recent_calls` (`limit: 5`).
   - A pattern: if the user asks about objections in general, use up to 5 recent completed calls from `list_recent_calls` (`days: 30`, `limit: 20`).
2. For each call, read `get_call_transcript` (`maxChars: 30000`) and `get_call_coaching`.
3. Find each objection: the moment the prospect pushed back, hesitated or deflected. For each one, capture:
   - **They said**: a short quote
   - **You said**: a short quote of the rep's reply
   - **What happened next**: did the conversation move forward, stall or end?
4. For each objection, give a better response in three parts: acknowledge it in the prospect's terms, ask one question that uncovers the real concern, then answer with something specific to this prospect. Write it the way the rep would say it out loud, in two to four sentences.
5. If you reviewed several calls, finish with the objection that came up most and the one habit that would help most across calls, tied to the coaching opportunities Amotions flagged.

Quote only what is in the transcript. If speakers are not labelled clearly, say which lines you assumed were the prospect. Offer a quick practice round: you play the prospect and raise the same objection, and give feedback after the user answers.

If the Amotions tools are not available, tell the user to connect Amotions AI from this plugin's Connectors tab, or paste the part of the call they want to work on.
