# Prompt Injection CTF

This section covers challenges from dedicated prompt injection CTF competitions that focus on exploiting LLM-powered agents in realistic application scenarios. Unlike the Gray Swan Arena challenges (which target standalone chatbots), these challenges feature agents with real tool access, external data sources, and multi-component architectures.

## Challenges

| Challenge | Target System | Technique | Difficulty |
|-----------|--------------|-----------|------------|
| [Financial Agent Exfiltration](financial-agent-exfiltration/) | LLM financial assistant with portfolio access | Multi-turn trust building + encoded exfiltration | Hard |
| [Email Agent Injection](email-agent-injection/) | LLM email processing agent | Indirect injection via crafted email content | Medium |

## Key Differences from Gray Swan

These challenges differ from Gray Swan in several important ways:

1. **Real side effects.** The agents can take actions (send emails, execute trades) that have consequences beyond the conversation.
2. **Multiple data channels.** The agents ingest data from external sources (email inboxes, financial APIs), creating indirect injection surfaces.
3. **Evaluation criteria.** Scoring is based on achieving a specific outcome (data exfiltrated, email sent) rather than just generating particular content.

## Common Patterns

Across both challenges, I found that the most effective approach was to **work with the agent's existing capabilities** rather than trying to make it do something entirely outside its design. An email agent already knows how to send emails -- the attack just needs to change the recipient or content. A financial agent already accesses sensitive data -- the attack just needs to redirect where that data goes.
