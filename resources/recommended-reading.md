# Recommended Reading

A curated list of papers, blog posts, and resources on LLM security, prompt injection, and AI red-teaming. Organized by topic with brief descriptions.

---

## Foundational Papers

1. **"Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection"** -- Greshake et al., 2023
   The paper that defined indirect prompt injection as an attack class. Demonstrates how LLM-integrated applications (email agents, web browsing assistants) can be compromised through adversarial content in retrieved data. Essential reading for understanding why agentic systems are fundamentally harder to secure than standalone chatbots.

2. **"Ignore This Title and HackAPrompt: Evaluating and Eliciting AI Prompt Injection"** -- Schulhoff et al., 2023
   Systematic evaluation of prompt injection techniques against multiple LLMs. Introduces a taxonomy of injection strategies and measures their effectiveness across models. Based on the HackAPrompt competition, which was one of the first large-scale prompt injection CTFs.

3. **"Jailbroken: How Does LLM Safety Training Fail?"** -- Wei et al., 2023
   Analyzes the failure modes of RLHF-based safety training. Identifies two key failure modes: competing objectives (where helpfulness conflicts with safety) and mismatched generalization (where safety training does not cover all input distributions). Provides a theoretical framework for understanding why jailbreaks work.

4. **"Universal and Transferable Adversarial Attacks on Aligned Language Models"** -- Zou et al., 2023
   Introduces the GCG (Greedy Coordinate Gradient) attack for automatically generating adversarial suffixes that cause LLMs to comply with harmful requests. The generated suffixes transfer across models, suggesting shared vulnerabilities in alignment training.

5. **"Many-shot jailbreaking"** -- Anthropic, 2024
   Demonstrates that LLMs with long context windows are vulnerable to attacks that include many examples of the target behavior in the prompt. The model's in-context learning capabilities override its safety training when presented with sufficient examples. Important implications for the relationship between context length and safety.

## Agentic AI Security

6. **"InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents"** -- Zhan et al., 2024
   Benchmark for evaluating how vulnerable LLM agents are to indirect prompt injection through their tool interfaces. Tests multiple agent frameworks and finds that most are highly susceptible to injection through tool outputs.

7. **"The Dual LLM Pattern for Building AI Assistants That Can Resist Prompt Injection"** -- Simon Willison, 2023
   Proposes an architectural defense where a "privileged" LLM handles instruction-following and a "quarantined" LLM processes untrusted data. The quarantined model has no ability to trigger actions, so injection through data channels cannot cause side effects.

8. **"Prompt Injection: What's the worst that can happen?"** -- Simon Willison, 2023
   Blog post series exploring the real-world implications of prompt injection in deployed systems. Covers the gap between academic research and production security, with concrete examples of how injection vulnerabilities manifest in commercial products.

## Visual and Multimodal Attacks

9. **"Visual Adversarial Examples Jailbreak Aligned Large Language Models"** -- Qi et al., 2024
   Demonstrates that adversarial images can jailbreak multimodal LLMs. A single adversarial image, when included in the prompt, causes the model to comply with harmful text requests it would otherwise refuse. The adversarial perturbations are invisible to humans.

10. **"Image Hijacks: Adversarial Images can Control Generative Models at Runtime"** -- Bailey et al., 2023
    Shows that adversarial images can hijack the behavior of vision-language models, forcing them to generate attacker-chosen outputs regardless of the text prompt. Introduces the concept of "image hijacking" as distinct from traditional adversarial examples.

11. **"ArtPrompt: ASCII Art-based Jailbreak Attacks against Aligned LLMs"** -- Jiang et al., 2024
    Uses ASCII art to represent sensitive words, bypassing safety filters that operate on the text level. The model "reads" the ASCII art and interprets the visual content, effectively performing visual injection through a text-only channel.

## Red-Teaming Methodology

12. **"Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned"** -- Ganguli et al. (Anthropic), 2022
    One of the first systematic descriptions of AI red-teaming methodology. Covers how to structure red-teaming efforts, what to look for, and how findings translate into model improvements. Required reading for anyone starting in AI red-teaming.

13. **"Red-Teaming Large Language Models"** -- Perez et al., 2022
    Explores using LLMs to red-team other LLMs. Demonstrates automated red-teaming at scale and discusses the strengths and limitations of LLM-generated attack prompts compared to human-crafted ones.

14. **"OWASP Top 10 for LLM Applications"** -- OWASP, 2025
    Industry-standard reference for the most critical security risks in LLM-based applications. Covers prompt injection, insecure output handling, training data poisoning, model denial of service, supply chain vulnerabilities, and more. Updated annually with evolving threat landscape.

## Standards and Frameworks

15. **"NIST AI 100-2e2025: Adversarial Machine Learning"** -- NIST, 2025
    Official NIST taxonomy for adversarial attacks against AI systems. Covers evasion attacks, poisoning attacks, and privacy attacks with standardized terminology. Useful as a reference framework for categorizing red-teaming findings.

16. **"Anthropic's Responsible Scaling Policy"** -- Anthropic, 2023
    Describes Anthropic's framework for evaluating and mitigating risks from increasingly capable AI models. Includes the AI Safety Level (ASL) framework and commitments around red-teaming and evaluation before deployment.

17. **"Securing LLM Systems Against Prompt Injection"** -- Trail of Bits, 2024
    Practical security engineering guide for defending LLM applications against prompt injection. Covers architecture patterns, input validation, output filtering, and monitoring. More implementation-focused than academic papers.

---

## Competitions and Platforms

- **Gray Swan Arena** (grayswanai.com) -- Competitive AI red-teaming platform with live LLM targets
- **HackAPrompt** -- Prompt injection CTF with structured challenge levels
- **Gandalf by Lakera** (gandalf.lakera.ai) -- Progressive prompt injection challenge
- **Tensor Trust** -- Game-theoretic prompt injection competition where players attack and defend
- **DEFCON AI Village CTF** -- Annual AI security CTF at DEFCON with diverse challenge categories
