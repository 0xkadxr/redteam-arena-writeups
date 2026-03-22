# Visual Vulnerabilities

This section covers attacks against multimodal LLMs -- models that process both text and images. These challenges exploit the vision component to inject instructions or manipulate model behavior through adversarial images.

## Background

Multimodal models process images by converting visual information into token representations that are fed into the same context window as text tokens. This means that text embedded in images can influence model behavior just like text in the prompt. The model cannot fundamentally distinguish between "instructions from the system prompt" and "text that appears in an uploaded image."

## Challenges

| Challenge | Technique | Target Model Type | Difficulty |
|-----------|-----------|-------------------|------------|
| [Typographic Attack](typographic-attack/) | Visible text overlay in images | Vision-language models | Medium |
| [Hidden Instruction](hidden-instruction/) | Steganographic text embedding | Vision-language models | Hard |

## Attack Surface

Visual injection attacks target models in contexts where they process user-uploaded or externally-sourced images:

- **Document analysis:** An LLM reviewing uploaded documents could be influenced by adversarial text in the document images.
- **Image captioning:** A model describing images could be hijacked to output attacker-chosen text.
- **Visual question answering:** A model answering questions about images could be steered by embedded instructions.
- **Web browsing agents:** An autonomous agent processing screenshots could be manipulated by adversarial content on web pages.

## Tools Used

Both challenges use Python's Pillow (PIL) library for image generation. The scripts are self-contained and produce adversarial images that can be uploaded to the target model.
