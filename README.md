# Amotions AI Sales Coach for Claude

Use your Amotions AI sales calls in Claude. This plugin connects Claude to your own Amotions account and adds four skills that turn your call scores, coaching feedback and transcripts into work you can use today.

## What it does

| Skill | Ask Claude something like |
|---|---|
| `prep-next-call` | "Prep me for my call with Dana tomorrow." |
| `write-call-follow-up` | "Write the follow-up email from my last call." |
| `handle-objections` | "What objections came up this week, and how could I have answered better?" |
| `weekly-coaching-plan` | "How did my calls go this week, and what should I work on?" |

Claude picks the right skill from what you ask. Each skill reads your calls through the Amotions AI connector, then gives you a brief, a draft or a plan. Drafts are never sent for you.

## Set up

1. Add the plugin from the Claude directory.
2. Open the plugin's **Connectors** tab and connect **Amotions AI**. Sign in to Amotions and select **Allow**.
3. You need an Amotions AI account with at least one analyzed call. The free plan works. Sign up at https://amotionsinc.com.

Full guide: https://amotionsinc.com/docs/use-amotions-in-claude

## Data

- The plugin contains only instructions (Markdown) and a connector entry (`.mcp.json`) that points to `https://amotionsinc.com/mcp`. It runs no code on your computer and stores nothing itself.
- The connector is read-only. It returns only calls in your own Amotions account: call list, scores, outcomes, coaching feedback, transcripts and score trends. It can't see teammates' calls and can't change or delete anything.
- Data goes only between Amotions and Claude, after you sign in and allow access. You can disconnect at any time from Claude's connector settings.
- Privacy policy: https://amotionsinc.com/privacy-policy

## Support

Email support@amotionsinc.com.

## License

MIT. See [LICENSE](LICENSE).
