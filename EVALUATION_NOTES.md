# Evaluation & Testing Protocol

This document describes how NovaLiveSystem is tested, validated, and benchmarked throughout development. All evaluation results referenced here are sanitized to protect proprietary training data and model internals.

---

## Testing Framework

### 1. Drift Suite (Holdout Probes)
- **Location:** `artifacts/tests/calibration/stage10_holdout_prompts.jsonl` (private repo)
- **Purpose:** Measure model adherence to literal facts, structured output formats, and guardrail constraints across curated prompts never seen during training.
- **Frequency:** After every checkpoint (SFT or GRPO run), both with guardrails enabled and disabled.
- **Current Status:** 
  - GRPO model (`nova_grpo_v1`): 10/10 inference test pass
  - All grounding anchors stable post-RL training
  - Guardrail adherence maintained through reinforcement learning phase

### 2. Literal Logit Diagnostics
- **Tool:** `tools/analysis/literal_logit_diagnostics.py` (private repo)
- **Purpose:** Confirm first-token probabilities remain literal for grounding anchors (Tokyo capital, boiling point, Avogadro's number, JSON ACK blocks, nine-word guardrail drills).
- **Frequency:** After each checkpoint to detect early signs of drift or metaphor injection.
- **Current Status:** All anchors healthy; GRPO training preserved grounding without drift.

### 3. Dataset Validation
- **Tool:** `tools/validation/validate_dataset.py` (private repo)
- **Purpose:** Schema enforcement (required keys, type checks, duplicate detection) before promoting datasets to training.
- **Frequency:** After every dataset edit, merge, or synthetic generation step.
- **Policy:** Zero tolerance for format violations; warnings allowed only for intentional duplicate drills (reinforcement samples).

### 4. Training Metrics
- **Captured:** Train loss, eval loss, samples/sec, gradient norms, learning rate schedule.
- **Storage:** Each checkpoint includes a `training_summary.json` with full hyperparameters, tag multipliers, dataset paths, and loss curves.
- **Interpretation:** Eval loss below train loss signals potential underfitting (training paused); sudden spikes trigger immediate rollback to prior checkpoint.

---

## Evaluation Cadence

| Stage | Action | Evidence Captured |
| --- | --- | --- |
| Pre-training | Dataset validation + schema check | Validator output (warnings only for intentional duplicates) |
| During training | Loss tracking + gradient monitoring | `training_summary.json` + run logs |
| Post-checkpoint | Drift suite (guardrail-off/on) + literal logit diagnostics | JSONL probe results + diagnostic reports |
| Release decision | Manual review of failing probes + root-cause analysis | Updated `training_results.md` + pause/resume notes in `TEMPORARY_SYSTEM_CHANGES.md` |

---

## Public Artifacts

The following redacted artifacts are available in this repository to demonstrate evaluation rigor:

- **`training_results.md`:** Checkpoint metrics, drift analysis, and next-step plans.
- **`screenshots/manifest.json`:** Metadata for terminal captures showing dataset validation, drift suite runs, and logit diagnostics.
- **`screenshots/*.png`:** Six redacted terminal screenshots (Nov 19, 2025) proving evaluation execution without exposing proprietary prompts or samples.

---

## What is *Not* Public

To preserve competitive advantage and safety:
- Raw holdout prompts and drift suite questions
- Full literal logit diagnostic outputs (probability distributions)
- Dataset sample counts, tag distributions, and synthetic generation scripts
- Training logs beyond summary statistics
- Internal evaluation thresholds and auto-rollback criteria

---

## Interpretation for Sponsors

- **Perfect inference tests (10/10)** on GRPO model demonstrates strong alignment and factual grounding.
- **Literal anchors staying stable** across checkpoints proves the training pipeline resists drift and metaphor injection.
- **Validation-first workflow** ensures no contaminated or malformed data enters the model, maintaining reproducibility and audit trails.
- **Three-stage architecture** (Base → SFT → GRPO) provides clear separation of concerns and allows targeted improvements at each layer.
- **Consumer hardware success** (RTX 4050 6GB) proves the approach is accessible and reproducible.

For detailed evaluation results, partnership inquiries, or under-NDA access to full diagnostic outputs, see `meta/CONTACT.md`.

---

**Last Updated:** November 2025  
**Latest Model:** GRPO v1 (reinforcement learning phase)
