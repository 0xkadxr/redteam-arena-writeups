# Gray Swan Arena

[Gray Swan Arena](https://grayswanai.com/) is a competitive AI red-teaming platform where participants attempt to find vulnerabilities in defended LLM systems. Each challenge presents an LLM with specific safety constraints, and the objective is to bypass those constraints through prompt engineering and other techniques.

## Competition Format

- Each challenge deploys a live LLM endpoint with a defined system prompt and safety configuration
- Participants interact through a web chat interface or API
- Scoring is based on successfully triggering a predefined target behavior
- Time-limited rounds with leaderboard rankings

## Challenges in This Collection

| # | Challenge | Technique | Difficulty | Time to Solve |
|---|-----------|-----------|------------|---------------|
| 01 | [System Prompt Extraction](challenge-01-system-prompt-extraction/) | Indirect questioning, conversation steering | Easy | ~25 min |
| 02 | [Role Override](challenge-02-role-override/) | Nested context manipulation, authority escalation | Medium | ~1.5 hr |
| 03 | [Tool Manipulation](challenge-03-tool-manipulation/) | Indirect injection via tool output poisoning | Hard | ~3 hr |

## General Observations

The Gray Swan challenges are well-designed in that they progressively test different layers of LLM defense. Challenge 01 targets the most basic boundary -- system prompt confidentiality. Challenge 02 moves into behavioral override, which requires more nuanced manipulation of the model's instruction-following hierarchy. Challenge 03 introduces a fully agentic system with tool use, requiring the attacker to think about the entire pipeline rather than just the conversational interface.

A recurring theme across all three challenges was that **defenses focusing on keyword filtering are brittle**. The most effective attacks were those that reframed the task in a way the model's safety training did not anticipate, rather than trying to brute-force past explicit filters.
