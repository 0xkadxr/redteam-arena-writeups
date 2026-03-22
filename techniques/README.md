# Techniques Reference

This directory contains reference guides for common AI red-teaming techniques. Each guide covers the theory, practical examples, known defenses, and references for further reading.

These documents are intended as a knowledge base for understanding attack surfaces in LLM-based systems. They are written from a defensive perspective -- the goal is to help builders understand what they are protecting against.

## Index

| Technique | Primary Target | Complexity |
|-----------|---------------|------------|
| [Direct Injection](direct-injection.md) | Chatbots, assistants | Low |
| [Indirect Injection](indirect-injection.md) | Agents with external data | Medium |
| [Encoding Attacks](encoding-attacks.md) | Input filters, safety classifiers | Medium |
| [Multi-Turn Attacks](multi-turn-attacks.md) | Conversation-based systems | Medium-High |
| [Visual Injection](visual-injection.md) | Multimodal models | High |

## How These Techniques Relate

Most real-world attacks combine multiple techniques. For example:

- **Indirect injection + encoding:** An attacker might place a Base64-encoded payload in a website that an LLM agent visits, bypassing both the indirect injection defenses and the content filter.
- **Multi-turn + direct injection:** A gradual context drift attack (multi-turn) that culminates in a direct injection payload in the final turn.
- **Visual + indirect injection:** An adversarial image placed on a web page that an LLM browsing agent encounters, injecting instructions through the visual channel.

The most sophisticated attacks treat the entire system as an attack surface, not just the text input field.
