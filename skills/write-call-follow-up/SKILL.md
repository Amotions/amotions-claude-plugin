---
name: write-call-follow-up
description: Write a follow-up email or message after a sales call recorded in Amotions AI. Use when the user asks for a follow-up, recap email, thank-you note, next-steps message or summary to send to a prospect or customer after a call.
---

# Write the call follow-up

1. Find the call. If the user didn't say which one, call `list_recent_calls` (`limit: 5`) and use the most recent completed call, naming it (date and score) so the user can correct you.
2. Call `get_call_transcript` (`maxChars: 40000`) for that call, and `get_call_coaching` for its summary and next-call actions.
3. From the transcript, pull only what was actually said:
   - the prospect's goals and pain points, in their words
   - questions you promised to answer, and materials you promised to send
   - the agreed next step, with its date and time if one was set
   - names, roles and numbers that came up
4. Write the email:
   - A subject line that names the next step or the prospect's goal, not "Following up".
   - Two to four short paragraphs or a short paragraph plus bullets: thank them for something specific, restate their goal, answer any open question, and confirm the next step with the date.
   - Plain, warm and specific. No filler such as "I hope this email finds you well" and no claims that were not discussed on the call.
5. After the draft, list anything you could not confirm from the transcript (for example a price, a date or an attachment) so the user can fill it in before sending.

Draft only. Never say the email was sent; the user sends it from their own email.

If the transcript is missing or still processing, say so, and offer to write from notes the user pastes in. If the Amotions tools are not available, tell the user to connect Amotions AI from this plugin's Connectors tab.
