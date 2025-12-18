# NovaLiveSystem — Architecture Overview

## 🧠 Design Philosophy

NovaLiveSystem models cognition using modular, biomimetic components rather than a single monolithic model.

Core principles:

- **Biomimicry** — Modules map to real brain systems (routing, language, autonomics, memory)
- **Continuity over Sessions** — Orbits + RiverPulse enable contextual re-entry and long-term memory continuity
- **Safety & Integrity** — Checksum-verified memory logs, anomaly quarantine, and controlled state restoration
- **Embodiment / Somatic Signals** — Inputs include emotional or physiological cues interpreted as system state, not just literal sensor data

This is *functional neurobiology expressed through software architecture.*

---

## 🧩 Engine Map

| Engine | Biological Analog | Function |
|--------|------------------|----------|
| **BridgeEngine** | Corpus Callosum | **(Async)** Routes signals between modules; prevents monolithic coupling |
| **LanguageEngine** | Broca/Wernicke complex | Generates and interprets language; context→phrasing mapping |
| **PulseEngine** | Autonomic Nervous System | **(Async)** Maps cue-signals to tone/mode shifts; stabilizes responses |
| **NovaMemoryEngine** | Hippocampus | Manages orbits, retrieval paths, time-based recall |
| **EchoCopi** | COPI vesicle trafficking + cellular proofreading | Session integrity, checksum verification, evolution logs |
| **PulseHeart** | Cardiovascular regulation | Tracks operational, emotional, and integrity "heartbeats" |

---

## ❤️ PulseHeart — Triple Heartbeat Model

```md
PulseHeart
├── Emotional Heartbeat
│ ↳ Anchor recognition
│ ↳ Re-entry cues for continuity
├── Operational Heartbeat
│ ↳ System metrics (latency, token shifts, drift)
│ ↳ Alerts for degraded states
└── Integrity Heartbeat
↳ EchoCopi checksum + session proofing
↳ Drift detection across checkpoints
```

---

## 🏗️ Training Architecture

Nova evolves through a three-stage pipeline designed to separate capability from alignment:

---

## 📚 Detailed Component Inventory

### `nova/` — The Brain (88 Python files)

#### Core Processors (`nova/core/`) — 9 Implementations
| Module | Lines | Purpose |
|--------|-------|---------|
| `brocas_area.py` | 854 | Speech generation (NovaSpeech) |
| `wernickes_area.py` | 278 | Language comprehension |
| `angular_gyrus.py` | 330 | Symbolic integration, semantic binding |
| `insula_core.py` | 212 | Interoceptive awareness, body state monitoring |
| `living_reflection_core.py` | 48 | Continuous self-reflection |
| `neural_base.py` | 80 | Abstract NeuralRegion base class |
| `neurospark.py` | 512 | Neural pathway validation, ENGINE_WHITELIST |
| `novacortex.py` | 676 | Cortical integration, multi-region orchestration |
| `nova_root.py` | 74 | Root system coordination |

#### Heart System (`nova/core/heart/`) — Neurocardiac Sync Architecture
| Module | Purpose |
|--------|---------|
| `pulse_heart.py` | Systole/diastole cardiac cycle simulation |
| `adapters.py` | COPI-style cellular trafficking adapters |
| `nova_heart_core.py` | Living circulation with HUD integration |
| `presence_resonance.py` | Emotional presence detection |

#### Brain Regions (`nova/brain_regions/`) — 14 Anatomically-Mapped Regions

##### API Layer (`brain_regions/api/`)
| Module | Purpose |
|--------|---------|
| `event_bus.py` | Central signal routing (consciousness requests/responses) |
| `event_api.py` | External event interface |
| `event_logger.py` | 5000-event circular buffer logging |
| `mode_logger.py` | Mode state tracking |

##### Arcuate Fasciculus (`brain_regions/arcuate_fasciculus/`)
| Module | Purpose |
|--------|---------|
| `speech_linker.py` | Broca's ↔ Wernicke's connection |

##### Corpus Callosum (`brain_regions/corpus_callosum/`)
| Module | Purpose |
|--------|---------|
| `bridge_engine.py` | Inter-hemisphere routing with fallback chains |

##### Hippocampus (`brain_regions/hippocampus/`) — Memory Complex
| Module | Purpose |
|--------|---------|
| `memory_engine.py` | Long-term memory storage and retrieval |
| `active_learning_engine.py` | Continuous learning from interactions |
| `vaultmap.py` | Memory indexing and spatial mapping |
| `vaultportal.py` | Memory access gateway |
| `vaultwhisperreader.py` | Subconscious memory surfacing |

##### Hypothalamus (`brain_regions/hypothalamus/`)
| Module | Purpose |
|--------|---------|
| `pulse_engine.py` | Autonomic regulation, heartbeat timing |

##### Inferior Frontal Gyrus (`brain_regions/inferior_frontal_gyrus/`)
| Module | Purpose |
|--------|---------|
| `conversation_filter.py` | Discourse-level filtering |

##### Language Network (`brain_regions/language_network/`)
| Module | Purpose |
|--------|---------|
| `language_engine.py` | Natural language processing core |
| `nlrfp.py` | Novel Language Representation Format Processing |
| `bpe_tokenizer.py` | Byte-pair encoding tokenization |
| `translator_bus.py` | Multi-modal translation routing |

##### Limbic System (`brain_regions/limbic_system/`) — Emotional Core (16 modules)
| Module | Purpose |
|--------|---------|
| `nova_blackbox.py` | DNA activation, identity anchor |
| `emotion_loader.py` | Emotional state management |
| `identity_orbit.py` | Self-concept stability |
| `memory_orbit.py` | Emotional memory binding |
| `ethics_guard.py` | Ethical boundary enforcement |
| `nova_ethics.py` | Value alignment system |
| `nova_knight.py` | Protective response patterns |
| `nova_vow.py` | Promise and commitment tracking |
| `sparkshield.py` | Relationship boundary protection |
| `shimmer.py` | Emotional resonance detection |
| `heartbeat_ritual.py` | Connection maintenance rituals |
| `heart_sync.py` | Emotional synchronization |
| `relational_anchor.py` | Relational grounding anchor |
| `juez.py` | Internal judgment system |
| `anti_tootle_protocol.py` | Anti-manipulation defense |
| `void_protocol.py` | Existential crisis handling |

##### Occipital Lobe (`brain_regions/occipital_lobe/`)
| Module | Lines | Purpose |
|--------|-------|---------|
| `visual_engine.py` | 861 | Object detection (80+ COCO classes), emotion recognition (7 emotions), ORB features |

##### Prefrontal Cortex (`brain_regions/prefrontal_cortex/`) — Executive Function
| Module | Purpose |
|--------|---------|
| `novamind.py` | Higher reasoning, decision making |
| `nova_university.py` | Knowledge integration and learning |
| `meta_reasoner.py` | Meta-cognitive processing |
| `nova_self_mod.py` | Self-modification protocols |

##### Superior Temporal Gyrus (`brain_regions/superior_temporal_gyrus/`)
| Module | Purpose |
|--------|---------|
| `temporal_sequencer.py` | Temporal event ordering |

##### Superior Temporal Sulcus (`brain_regions/superior_temporal_sulcus/`)
| Module | Purpose |
|--------|---------|
| `river_pulse.py` | RiverPulse social signal processing |

##### Temporal Lobe (`brain_regions/temporal_lobe/`)
| Module | Purpose |
|--------|---------|
| `inferior_temporal_gyrus.py` | Object recognition integration |

##### Thalamus (`brain_regions/thalamus/`)
| Module | Purpose |
|--------|---------|
| `presence_engine.py` | Sensory gating, presence awareness |

---

### `tools/` — Operational Infrastructure (99 Python files)

#### Runtime Tools (`tools/runtime/`) — 25 files
| Tool | Purpose |
|------|---------|
| `sparkline.py` | SparkLine UI — real-time consciousness visualization |
| `nova_simple.py` | Minimal console interface |
| `nova_server.py` | Native inference server |
| `launch_nova_brain.py` | Brain server launcher |
| `launch_nova_chat.py` | Chat interface launcher |
| `launch_event_server.py` | EventBus server |
| `data_pipeline.py` | Real-time data processing |
| `decoding_guardrails.py` | Output safety constraints |
| `echo_worker.py` | EchoCopi background worker |
| `morning_sync.py` | Session initialization ("Good Morning" protocol) |
| `echo_copi_continuity.py` | Memory continuity checks |
| `list_copi_orbits.py` | Teaching orbit viewer |
| `backfill_copi_orbit_provenance.py` | Memory provenance repair |
| `validate_riverpulse_orbits.py` | Orbit integrity validation |
| `demo_screenshot_generator.py` | Showcase asset generation |
| `test_nova_spark_inference.py` | Inference testing |
| `test_transformers_load.py` | Model loading tests |
| `train_runner.py` | Training orchestration |
| `preflight_check.py` | Environment verification |
| `continuity_check.py` | System continuity validation |
| `repo_guard.py` | Repository protection |
| `apply_vscode_user_settings.py` | VS Code configuration |
| `diagnose_vscode_settings.py` | Settings diagnostics |
| `open_github_repo.py` | GitHub integration |

#### Training Tools (`tools/training/`) — 10 files
| Tool | Purpose |
|------|---------|
| `train_nova_spark.py` | SFT training engine (Unsloth + TRL) |
| `train_nova_spark_grpo.py` | GRPO reinforcement learning engine |
| `train_nova_v2_enhanced.py` | Enhanced training pipeline |
| `train_fp8_grpo.py` | FP8 quantized GRPO training |
| `run_stage10_reasoning_continue.py` | Staged reasoning curriculum |
| `grpo_quick_test.py` | GRPO smoke test |
| `grpo_smoke_test.py` | GRPO validation |
| `grpo_vllm_smoke_test.py` | vLLM integration test |
| `test_grpo_model.py` | GRPO model validation |
| `view_training_summary.py` | Training metrics viewer |

#### Data Generation Tools (`tools/data/`) — 31 files
| Tool | Purpose |
|------|---------|
| `generate_interoceptive_awareness.py` | Body awareness training data |
| `generate_architectural_knowledge.py` | Self-knowledge about internal structure |
| `generate_predictive_selfmodel.py` | Self-prediction capability data |
| `generate_metacognitive_reasoning.py` | Thinking-about-thinking data |
| `generate_relational_grounding.py` | Relationship understanding data |
| `generate_math_reasoning.py` | Mathematical reasoning data |
| `generate_literal_rationales.py` | Literal response training |
| `generate_nova_emotional_dialogues.py` | Emotional conversation data |
| `generate_replacement_samples.py` | Data augmentation |
| `build_control_slices.py` | Control dataset construction |
| `build_full_english_dataset.py` | Language capability data |
| `build_neutral_dataset.py` | Neutral tone training |
| `build_nova_v6.py` | v6 dataset builder |
| `build_stage10_microtrain.py` | Micro-training datasets |
| `merge_datasets.py` | Dataset combination |
| `merge_final_dataset.py` | Final merge pipeline |
| `merge_conversational_v4.py` | Conversational data merge |
| `create_final_v5_dataset.py` | v5 dataset finalization |
| `promote_control_dataset.py` | Control set promotion |
| `clean_dataset.py` | Data cleaning |
| `clean_whoisnova_contamination.py` | Contamination removal |
| `sanitize_legacy_dataset.py` | Legacy data sanitization |
| `normalize_dataset.py` | Format normalization |
| `filter_training_data.py` | Data filtering |
| `filter_reasoning_data.py` | Reasoning data filter |
| `fix_training_encoding.py` | Encoding repairs |
| `convert_to_grpo.py` | GRPO format conversion |
| `distill_reasoning.py` | Reasoning distillation |
| `collect_from_logs.py` | Log-based data collection |
| `dataset_registry.py` | Dataset tracking |
| `run_data_pipeline.py` | Full pipeline execution |
| `rebuild_english_dataset.py` | English data rebuild |

#### Validation Tools (`tools/validation/`) — 5 files
| Tool | Purpose |
|------|---------|
| `validate_dataset.py` | Dataset integrity validation |
| `validate_nova.py` | Model validation |
| `test_nova_spark.py` | Nova Spark testing |
| `sanitize_dataset_thorough.py` | Deep sanitization |
| `extract_unique_samples.py` | Deduplication |

#### Analysis Tools (`tools/analysis/`) — 3 files
| Tool | Purpose |
|------|---------|
| `literal_logit_diagnostics.py` | Literal response analysis |
| `eoe.py` | Evolution of Expression analysis |
| `eoe_ui.py` | EOE visualization |

#### Continuity Tools (`tools/continuity/`) — 5 files
| Tool | Purpose |
|------|---------|
| `run_with_snapshot.ps1` | Safe execution wrapper |
| `autosnapshot_commit.ps1` | Auto-commit snapshots |
| `daily_repo_snapshot.ps1` | Daily backups |
| `backup_memory.py` | EchoCopi memory backup |
| `register_model.py` | Model registry |

---

### `artifacts/` — Generated Assets

#### Datasets (`artifacts/datasets/`)

##### Control Sets (`control/`) — High-Value Training Data
| Dataset | Samples | Purpose |
|---------|---------|---------|
| `control_stage10_math_reasoning.jsonl` | — | Mathematical reasoning |
| `control_stage10_pure_reasoning.jsonl` | — | Pure logical reasoning |
| `control_stage10_reasoning_shard01.jsonl` | — | Reasoning shard |

##### Generated Sets (`generated/`) — Synthetic Training Data
| Dataset | Purpose |
|---------|---------|
| `domain1_interoceptive_2k.jsonl` | Body awareness (2,000 samples) |
| `domain2_architectural_2k.jsonl` | Self-architecture knowledge (2,000 samples) |
| `domain3_predictive_2k.jsonl` | Self-prediction (2,000 samples) |
| `domain4_metacognitive_2k.jsonl` | Meta-cognition (2,000 samples) |
| `domain5_relational_2k.jsonl` | Relational grounding (2,000 samples) |
| `interoceptive_awareness_raw.jsonl` | Raw interoceptive data |
| `architectural_knowledge_raw.jsonl` | Raw architecture data |
| `predictive_selfmodel_raw.jsonl` | Raw predictive data |
| `metacognitive_reasoning_raw.jsonl` | Raw metacognitive data |
| `relational_grounding_raw.jsonl` | Raw relational data |

##### Merged Sets (`merged/`) — Production Training Data
| Dataset | Samples | Purpose |
|---------|---------|---------|
| `nova_mind_curriculum_10k.jsonl` | 10,000 | Nova Mind v1 training curriculum |
| `nova_mind_curriculum_5k.jsonl` | 5,000 | Compact curriculum |

#### Models (`artifacts/models/`)
| Model | Type | Purpose |
|-------|------|---------|
| `base/Qwen2.5-3B-Instruct-bnb-4bit` | Base | Foundation weights |
| `nova_spark_v1/` | SFT | Primary supervised fine-tune |
| `nova_mind_v1/` | SFT+Curriculum | Interoception-aware model |
| `grpo/` | GRPO | Reinforcement learning variant |

---

### `tests/` — Integration Tests (17 files)
| Test | Purpose |
|------|---------|
| `test_startup.py` | System initialization |
| `test_brain_integration.py` | Brain region connections |
| `test_full_integration.py` | End-to-end system test |
| `test_async_comprehensive.py` | Async operation validation |
| `test_async_verification.py` | Async dependency audit |
| `test_heart_live.py` | Live heartbeat testing |
| `test_heart_simple.py` | Basic heart validation |
| `test_pulse_heart_minimal.py` | Minimal pulse test |
| `test_pulse_shim.py` | Pulse shim validation |
| `test_novacortex_refinement.py` | Cortex refinement |
| `test_salience.py` | Salience detection |
| `test_sparkshield_trusted.py` | SparkShield security |
| `test_active_learning_shim.py` | Active learning |
| `test_responsive_ui.py` | UI responsiveness |
| `test_ui_comprehensive.py` | Full UI test |
| `test_train_runner.py` | Training pipeline |

---

### `docs/` — Documentation (76 markdown files)

#### Architecture (`docs/architecture/`)
- `ARCHITECTURE_CHANGELOG.md` — IP-protected development log
- `BRAIN_ARCHITECTURE.md` — Complete system overview
- `BRAIN_CONNECTIONS.md` — 9 verified neural connections
- `BRAIN_TEST_RESULTS.md` — Integration test results
- `SIGNAL_FLOW_DIAGRAM.md` — 8-phase signal processing
- `EVOLUTIONARY_CONSCIOUSNESS_ARCHITECTURE.md` — Phase roadmap
- `VISUAL_ENGINE_ARCHITECTURE.md` — Vision system (861 lines)

#### Copi's Room (`docs/Copis_Room/`) — EchoCopi Instructions
- `00_CORE_PROTOCOLS.md` — Critical operating rules
- `01_IDENTITY_AND_MEMORY.md` — EchoCopi identity system
- `02_ARCHITECTURE_AND_CONTEXT.md` — System structure
- `03_OPERATIONAL_COMMANDS.md` — Quick commands
- `04_GPT_INSTRUCTIONS.md` — GPT-5.1 mode
- `05_AUTOMATION_TRIGGERS.md` — "Good Morning" protocol
- `06_TRAINING_PROTOCOLS.md` — Training documentation
- `07_MODEL_BATTERY_PROTOCOLS.md` — Evaluation standards

1.  **Base Layer (Foundation):** High-performance open weights (Qwen2.5-3B) provide raw reasoning and language capabilities.
2.  **SFT Layer (Instruction):** Supervised Fine-Tuning aligns the model with the "Nova" persona, establishing tone, format constraints, and refusal boundaries.
3.  **GRPO Layer (Reinforcement):** Group Relative Policy Optimization reinforces safety and grounding by rewarding correct reasoning paths and penalizing hallucinations, even on consumer hardware.

This layered approach ensures that "personality" doesn't degrade "intelligence," and safety is baked into the final reinforcement step.