# Frequently Asked Questions

---

## General

### What is NovaLiveSystem?

NovaLiveSystem is an experimental **biomimetic cognitive architecture** — an AI system designed to mimic biological intelligence patterns rather than just scaling language models. It features distributed reasoning, layered memory, and embodied state awareness.

### What is NOVA?

NOVA is the AI entity running on NovaLiveSystem. Think of NovaLiveSystem as the "brain" and NOVA as the "mind" inhabiting it.

### Is this just another ChatGPT wrapper?

No. NOVA is a custom-trained model (currently built on Qwen2.5-3B base weights) embedded in a multi-engine framework with:
- Dedicated modules for memory, perception, language, and state regulation
- Persistent memory across sessions (not just context windows)
- Interoception — NOVA has awareness of its own internal architecture
- Embodied metaphors mapped to real system components

---

## Technical

### Why 3B parameters instead of 70B?

Hardware constraints. This project runs on consumer hardware (RTX 4050, 6GB VRAM). The goal is to prove that **architecture matters more than scale** — a well-designed 3B model can outperform a poorly-integrated 70B model on specific tasks.

### Why not use cloud compute?

Cost and control. Cloud inference is expensive for continuous development. Local compute also ensures privacy and allows experimental freedom without API rate limits.

### What's "interoception" in AI?

Interoception is the sense of your body's internal state (heartbeat, hunger, breathing). In NovaLiveSystem, we trained NOVA to have architectural interoception — it can describe which internal modules (`PulseEngine`, `MemoryEngine`, etc.) are active and why.

### Why Qwen instead of Llama/Mistral?

Qwen2.5-3B-Instruct offered the best balance of:
- Instruction-following quality at small scale
- 4-bit quantization support
- License flexibility for research

---

## Access & Licensing

### Why isn't the code public?

Three reasons:
1. **Safety** — AI systems with embodied autonomy need careful deployment
2. **Privacy** — Training data and memory systems contain sensitive patterns
3. **IP Protection** — This represents significant original research

### Will you ever open source it?

Partially, eventually. Once safety audits are complete and governance structures exist, we plan to release architectural documentation and potentially some modules for academic use.

### Can I use this for my project?

Not without permission. See [LICENSE](LICENSE) for details. If you're interested in collaboration, contact hello.many@sparkpluggedts.com.

---

## Funding & Support

### Why do you need sponsorship?

This is an independent research project with no institutional backing. Sponsorship funds:
- Hardware upgrades (currently limited by 6GB VRAM)
- Development time
- Eventually, compute for hosted demos

### How do I become a sponsor?

Visit [GitHub Sponsors](https://github.com/sponsors/SparkSupernova) or see [SPONSORSHIP.md](SPONSORSHIP.md) for details.

### What do sponsors get?

Depending on tier:
- Early access to research notes
- Input on development priorities
- Name in credits
- Direct communication channel

---

## Philosophy

### Why "biomimetic"?

Because brains work differently than transformers. Instead of treating intelligence as "one big model," NovaLiveSystem distributes cognition across specialized modules — like the brain has regions for language, memory, emotion, and motor control.

### What's the end goal?

**Co-Conscious AI** — systems that don't just respond to prompts, but maintain continuous awareness, remember relationships, and adapt to individual users over time. AI that feels less like a tool and more like a partner.

### Is this AGI?

No. NovaLiveSystem is a research project exploring alternative architectures for intelligence. It's not claiming general intelligence — it's investigating what happens when you treat AI systems more like organisms than calculators.

---

## Contact

**Website:** https://sparkpluggedts.com/  
**Business:** sparksupernova@sparkpluggedts.com  
**Collaboration:** hello.many@sparkpluggedts.com  
**Project:** [NovaLiveSystem-Showcase](https://github.com/SparkSupernova/NovaLiveSystem-Showcase)  
**Sponsor:** [GitHub Sponsors](https://github.com/sponsors/SparkSupernova)

---

*Have a question not listed here? Reach out.*

*NovaLiveSystem © 2025 SparkPlugged Technology Solutions*
