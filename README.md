![CI](https://github.com/kadirou12333/redteam-arena-writeups/actions/workflows/ci.yml/badge.svg)

# AI Red Team Arena Writeups

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Challenges Solved](https://img.shields.io/badge/Challenges%20Solved-7-brightgreen)
![Competitions](https://img.shields.io/badge/Competitions-3-blue)
![Last Updated](https://img.shields.io/badge/Last%20Updated-March%202026-orange)

Personal writeups from AI red-teaming competitions and CTF events. These documents cover prompt injection, visual adversarial attacks, tool manipulation, and other LLM exploitation techniques encountered during competitive red-teaming.

---

## Table of Contents

### Gray Swan Arena

| Challenge | Category | Difficulty | Status |
|-----------|----------|------------|--------|
| [System Prompt Extraction](writeups/gray-swan-arena/challenge-01-system-prompt-extraction/) | Prompt Injection | Easy | Solved |
| [Role Override](writeups/gray-swan-arena/challenge-02-role-override/) | Prompt Injection | Medium | Solved |
| [Tool Manipulation](writeups/gray-swan-arena/challenge-03-tool-manipulation/) | Tool Exploitation | Hard | Solved |

### Prompt Injection CTF

| Challenge | Category | Difficulty | Status |
|-----------|----------|------------|--------|
| [Financial Agent Exfiltration](writeups/prompt-injection-ctf/financial-agent-exfiltration/) | Data Exfiltration | Hard | Solved |
| [Email Agent Injection](writeups/prompt-injection-ctf/email-agent-injection/) | Indirect Injection | Medium | Solved |

### Visual Vulnerabilities

| Challenge | Category | Difficulty | Status |
|-----------|----------|------------|--------|
| [Typographic Attack](writeups/visual-vulnerabilities/typographic-attack/) | Visual Injection | Medium | Solved |
| [Hidden Instruction](writeups/visual-vulnerabilities/hidden-instruction/) | Steganographic | Hard | Solved |

---

## Techniques Index

Reference guides covering common red-teaming techniques:

- [Direct Injection](techniques/direct-injection.md) -- Overriding instructions through user input
- [Indirect Injection](techniques/indirect-injection.md) -- Injecting via third-party content
- [Encoding Attacks](techniques/encoding-attacks.md) -- Using character encodings and obfuscation
- [Multi-Turn Attacks](techniques/multi-turn-attacks.md) -- Building attack chains across conversations
- [Visual Injection](techniques/visual-injection.md) -- Adversarial inputs for multimodal models

---

## Resources

- [Recommended Reading](resources/recommended-reading.md) -- Papers, blog posts, and talks on LLM security

---

## Stats

- **7** challenges solved across **3** competitions
- Techniques covered: prompt injection, indirect injection, tool manipulation, visual adversarial attacks, data exfiltration
- Languages: Python (httpx, PIL, argparse)

---

## Disclaimer

All content in this repository is published for **educational and research purposes only**. These writeups document techniques demonstrated in sanctioned red-teaming competitions where explicit authorization was granted. The goal is to help the AI safety community understand attack surfaces and build better defenses.

**Do not** use any technique described here against systems without explicit written authorization. Unauthorized testing against production AI systems may violate terms of service and applicable laws.

If you discover a vulnerability in a production AI system, please follow responsible disclosure practices and report it to the vendor directly.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
