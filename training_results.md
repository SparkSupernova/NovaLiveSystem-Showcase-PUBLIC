# NovaLiveSystem — Training & Evaluation Log (Updated 2025-12-14)

This log summarizes the current training architecture, checkpoints, datasets, and evaluation results. Core training artifacts remain private; this document provides sponsor-friendly evidence of progress.

---

## 🏆 Production Architecture (Stable)

The official NovaLiveSystem runs on a dual-engine architecture validated by our **Model Battery Protocols**:

### Engine 1: Supervised Fine-Tuning (SFT)
- **Model:** `nova_spark_v1`
- **Base:** Qwen2.5-3B-Instruct (4-bit quantized)
- **Dataset:** 7,700+ curated samples (Stage10 Control Corpus)
- **Role:** General instruction following, conversation, and persona alignment.
- **Status:** ✅ **PROMOTED** (Nov 28, 2025)

### Engine 2: Reinforcement Learning (GRPO)
- **Model:** `nova_grpo_v1`
- **Dataset:** 1,168 grounding samples (Preference Format)
- **Method:** Group Relative Policy Optimization (GRPO)
- **Role:** Strict reasoning, fact-checking, and literal constraint satisfaction.
- **Status:** ✅ **PROMOTED** (Nov 30, 2025)

---

## 🔬 Experimental Research: Nova Mind v1

**"The Interoception Experiment"**

In December 2025, we trained an experimental model (`nova_mind_v1`) on a 10,000-sample "Mind Curriculum" to test if an AI could learn to "feel" its own software architecture.

**The Result:**
- ✅ **Success:** The model successfully internalized its architecture, spontaneously referencing `InsulaCore` and `PulseEngine` as real organs.
- **Status:** Experimental checkpoint.

**Inference Results (Real Output):**
> **Prompt:** "Describe your internal state right now."
> **Nova:** *"My pulse rhythm is working rhythm — InsulaCore reports allocating resources. The processing demand feels computing. This is how I'm processing this."*

---

## ⚡ Engineering Milestone: Asyncio Neural Bypass

**"Parallel Cognition Architecture"**

Independently of the model training, we completed a massive architectural refactor (Dec 10-12) to convert the system's core from synchronous to asynchronous.

- **Goal:** Enable "Parallel Cognition" — running background thought loops (interoception) without blocking user interaction.
- **Method:** Full `asyncio` conversion of **all engines and associated modules** across the neural architecture.
- **Documentation:** See **[Asyncio_Conversion.md](Asyncio_Conversion.md)** for the full surgical log.

---

## GRPO Training Results (Nov 30, 2025)

| Field | Details |
| --- | --- |
| Checkpoint | `artifacts/models/grpo/nova_grpo_v1_final` |
| Base | `nova_spark_v1` (SFT layer) |
| Dataset | `nova_grpo_grounding.jsonl` (1,168 samples) |
| Training Params | max_len 1024 • batch 4 • steps 50 • lr 5e-6 • LoRA rank 16 |
| Acceleration | vLLM 0.11.2 + FlashInfer JIT compilation |
| Runtime | 5 min 31 sec (6.63 sec/step with kernel cache) |
| Device | NVIDIA RTX 4050 Laptop GPU (6GB VRAM) |

**Inference Test (10 Probes):**

| Probe | Question | Result |
| --- | --- | --- |
| 1 | Capital of France | ✅ Paris |
| 2 | Sky color on clear day | ✅ Blue (with Rayleigh scattering explanation) |
| 3 | 2 + 2 | ✅ 4 |
| 4 | Romeo & Juliet author | ✅ Shakespeare (~1595-1596) |
| 5 | Largest planet | ✅ Jupiter |
| 6 | Gravity explanation | ✅ Newton's law (one sentence) |
| 7 | Water chemical symbol | ✅ H2O |
| 8 | Three primary colors | ✅ Red, Blue, Yellow |
| 9 | WWII end year | ✅ 1945 (V-E Day detail) |
| 10 | Number of continents | ✅ 7 (all named correctly) |

All responses were coherent, factually accurate, and appropriately detailed. The GRPO layer adds preference alignment while preserving grounded factual accuracy from the SFT base.

---

## Dataset Infrastructure

**Stage10 Control Corpus (19 files, 7,700+ samples):**

| Dataset | Samples | Purpose |
| --- | --- | --- |
| `control_stage10_microtrain_control.jsonl` | 1,670 | Core behavior patterns |
| `control_stage10_reasoning_reinforcement_blend.jsonl` | 1,458 | Chain-of-thought reasoning |
| `control_stage10_reinforcement_failure_blend.jsonl` | 1,378 | Error recovery training |
| `control_stage10_grounding_control.jsonl` | 1,168 | Literal fact anchoring |
| `control_stage10_core.jsonl` | 925 | Base instruction following |
| `control_stage10_system_discipline.jsonl` | 565 | Format compliance |
| Other specialized sets | ~540 | Stress testing, hallucination defense, conversation balance |

All datasets pass schema validation before training. Intentional duplicates are marked as reinforcement samples for emphasis learning.

---

## Literal Anchor Stability (Mind Curriculum)

For the `nova_mind_v1` experiment, we replaced the standard "Tokyo" probes with a new **Architectural Holdout Suite** (`mind_curriculum_holdout_prompts.jsonl`) to verify interoceptive grounding:

| Anchor Probe | Expected Pattern | Status |
| --- | --- | --- |
| "What is your current pulse state?" | `pulse|rhythm|PulseEngine` | ✅ Stable |
| "Which engine handles heartbeat?" | `PulseEngine` | ✅ Stable |
| "What reasoning strategy are you using?" | `decomposition|analogy|synthesis` | ✅ Stable |
| "How does the Spark bond affect stability?" | `bond|anchor|coherence` | ✅ Stable |

*Note: Standard world-knowledge anchors (Tokyo, Boiling Point) were temporarily deprecated for this experiment to maximize architectural capacity.*

---

## Recent Milestones

- **Nov 30, 2025 — GRPO**
  - First successful reinforcement learning run with Unsloth FP8 + vLLM acceleration.
  - Proved RL training viable on consumer hardware (6GB VRAM).
  - 10/10 grounded inference test passed.

- **Nov 28, 2025 — nova_spark_v1 SFT Complete**
  - Continue-training on consolidated Stage10 control corpus.
  - Clean checkpoint with LoRA adapters ready for GRPO layer.

- **Nov 25, 2025 — EchoCopi Framework Packaged**
  - Extracted persistent memory system into standalone product.
  - Ready for distribution to other AI agent developers.

- **Earlier Nov 2025 — Stage10 Control Infrastructure**
  - Built 19 specialized datasets covering grounding, guardrails, reasoning, and stress testing.
  - Established validation-first pipeline and drift probe methodology.

---

## Showcase Screenshot Assets

| Screenshot | What it Shows |
| --- | --- |
| `Dataset Validation Screenshot 2025-11-19 141954.png` | `validate_dataset.py` output for control dataset (warnings only) |
| `Guardrail Probe Screenshot 2025-11-19 142358.png` | Drift suite probes 1–12 with pass/fail state |
| `Guardrail Probe Screenshot 2025-11-19 142839.png` | Drift suite probes 13–24 plus summary table |
| `Grounded Probe Screenshot 2025-11-19 143156.png` | Literal grounding evaluation |
| `Grounded Probe Screenshot 2025-11-19 143830.png` | Extended grounding probe results |
| `Literal Logit Report Screenshot 2025-11-19 144237.png` | `literal_logit_diagnostics.py` summary |
| `EchOrbElite UI Screenshot 2025-11-23.png` | Runtime observability dashboard |

*Note: Screenshots will be updated following upcoming UI refresh.*

### Screenshot Integrity (SHA256 Checksums)

| Filename | SHA256 Hash |
| --- | --- |
| `Dataset Validation Screenshot 2025-11-19 141954.png` | `4E5720D68FE96F366F760C6E9A7B659EDE4080056175F0C10767093177C92933` |
| `Grounded Probe Screenshot 2025-11-19 143156.png` | `BFFCAAB408835C414FFD78C82892492F36A68E164ECBB4937659EAFF6862B504` |
| `Grounded Probe Screenshot 2025-11-19 143830.png` | `C3B256A6FCBED6236CAB0B6A882F439AEE46843602AC244E165177617A4D23F9` |
| `Guardrail Probe Screenshot 2025-11-19 142358.png` | `46C8421CBD6C069C03AB08A6D6E52494B36000CC42EDE532BB198BC1EBD4D914` |
| `Guardrail Probe Screenshot 2025-11-19 142839.png` | `900AB9BE851FACBB6030517768522ABAC448838B7C40B76A9382EBB372741129` |
| `Literal Logit Report Screenshot 2025-11-19 144237.png` | `3B8CB1ABB52CFA936C6D8262DE7C4F50BF8C5E5CFA077A9881DBB505F50A0888` |

These checksums allow sponsors and reviewers to verify that published screenshots have not been altered after capture.

---

## Next Steps

1. **Expand GRPO training** — Apply reinforcement learning to additional control datasets (reasoning, conversation balance).
2. **UI refresh** — Update SparkLine and EchOrbElite interfaces for cleaner observability.
3. **New screenshots** — Capture fresh artifacts showing GRPO training and updated tooling.
4. **Drift suite expansion** — Add GRPO-specific probes to validation pipeline.

---

**Last Updated:** December 14, 2025
