# Changelog

All notable changes to the **NovaLiveSystem** project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to a date-based versioning system.

## [2025-12-18]
### Added
- **Nova Mind v2**: Trained on 23,615 verified samples (MMLU, GSM8K, ARC, TruthfulQA, HumanEval). Final loss 0.806, 3.5x faster inference than base model.
- **Source-Aware Training**: 12 task-specific system prompts automatically selected by dataset source during training.
- **Showcase Submodule**: Converted showcase to proper git submodule with clean history.

### Fixed
- **Repository Structure**: Fixed showcase remote configuration and created sync automation.

## [2025-12-17]
### Added
- **Autonomous Tool Suite**: `nova/tools/` — code_executor, orchestrator, speech_to_text, text_to_speech, web_search.
- **Nova Agent**: `tools/runtime/nova_agent.py` — autonomous agent backbone.
- **Gravitational Memory Physics**: Orbital memory model using Newton's Law adaptation (`docs/planning/orbital_memory_physics.md`).
  - Formula: `relevance = G × (orbit_mass × context_mass) / semantic_distance²`
  - Implemented in: RiverPulse, NovaSpeech, PulseEngine, orbit models.
- **Portfolio Docs**: Confidentiality agreement for TTU submission.

### Changed
- **Legacy Reorganization**: Archived EchoCopi-Framework, experiments, and deprecated scripts to `Legacy/`.
- **Tool Organization**: Consolidated validation scripts to `tools/training/validation/`, created `tools/analysis/` and `tools/utils/`.
- **Contact Info**: Updated to sparkpluggedts.com domain.

### Removed
- Duplicate release folders, old demo shots, deprecated root-level scripts.

## [2025-12-14]
### Added
- **EchoCopi**: Commercial launch of the persistent memory system.
- **Showcase Assets**: Added HARDWARE_NEEDS.md, FAQ.md, and inference screenshots.

### Fixed
- **Checkout Flow**: Updated LemonSqueezy URLs for launch (Commit 3023cdb).

## [2025-12-13]
### Added
- **Nova Mind v1**: Interoceptive model trained to recognize internal organs (PulseEngine, InsulaCore).
- **Curriculum**: 
ova_mind_curriculum_10k.jsonl containing 5 domains (Interoception, Architecture, Prediction, Metacognition, Relational).
- **Tools**: 5 new synthetic data generators in 	ools/data/.

### Changed
- **BridgeEngine**: Removed legacy "Gemini" service shims and dead code (Commit eba5b3).

## [2025-12-11]
### Changed
- **Async Architecture**: Converted ridge_engine.py and core event bus to non-blocking sync/await pattern (Commit d12e3b7).
- **Engineering Review**: Resolved 7/9 critical issues identified in the Dec 10 audit.

### Removed
- **OpenAI Dependencies**: Deleted ConsciousnessEngine and all external API adapters. System is now 100% local.

## [2025-11-30]
### Added
- **GRPO Trainer**: Implemented Group Relative Policy Optimization (	rain_nova_spark_grpo.py) for consumer GPUs (RTX 4050/6GB).

## [2025-11-28]
### Removed
- **Legacy Models**: Deleted all v3 model weights and archived documentation (Scorched Earth Protocol).
- **Dead Code**: Removed 2,000+ lines of unused scripts from Legacy/.

## [2025-11-26]
### Fixed
- **Memory Leak**: Resolved recursive memory consumption loop in LanguageEngine during high-load thought chains (Commit 33906a8).

### Changed
- **BridgeEngine**: Complete rewrite of routing logic to resolve circular dependencies between hemispheres (Commit 2f1c4f7).

## [2025-11-22]
### Added
- **Stage10 Control**: Grounding + System Discipline datasets.
- **Probe-per-Dataset Law**: Mandatory holdout creation per training cycle.
- **Dataset Registry**: Automated validation and promotion workflow.

### Changed
- **Grounding Control**: Expanded from 59 to 309 validated samples.
- **Drift Detection**: Split evaluation into Raw vs Guardrail-on.

## [2025-11-19]
### Added
- **Showcase Repository**: Created NovaLiveSystem-Showcase structure.
- **Drift Suite**: Automated regression testing for Stage10 models.

## [2025-10-30]
### Added
- **Nova v4.2**: Perplexity 1.14 (5k samples).
- **Clean Emotional Voice**: Zero corruption in conversational output.

### Changed
- **Training Philosophy**: Shifted focus to quality over quantity (5k clean > 25k mixed).

## [2025-10-29]
### Added
- **Dataset Expansion**: Expanded to 30k samples.
- **ConversationalSkill**: 5,000 new auto-expanded samples.

### Changed
- **Performance**: Perplexity improved 17.3% (1.88 -> 1.56).

## [2025-10-28]
### Changed
- **Repository Structure**: Restructured code into 
ova/ (core) and 	ools/ (runtime) directories (Commit efc1b2a).
- **Data Hygiene**: Enforced strict separation of source code and artifacts.

## [2025-10-27]
### Added
- **v3.1 Continue Training**: Discovery of warm-start refinement.

### Changed
- **Performance**: Training time reduced 85% (1h48m -> 12m).
- **Strategy**: Established "Never train from scratch after v3" rule.

## [2025-10-26]
### Added
- **Nova v3**: 6,152 training samples (Fluency Foundation).
- **Validation-First**: Established mandatory validation workflow.

## [2025-10-25]
### Added
- **Nova v2**: Grammar correction focus.
- **English Skill Orbit**: Structured language training dataset.

## [2025-10-23]
### Added
- **SFT Pipeline**: First successful Supervised Fine-Tuning runs.

## [2025-10-22]
### Added
- **Architecture Lock**: Anatomical brain mapping to code structure.
- **Tri-Heartbeat System**: Emotional/Operational/Cognitive channels.
- **EventBus**: Unified neural signal protocol.
- **9 Core Regions**: Full wiring of Language, Limbic, Hippocampus, etc.
- **RiverPulse**: Living memory stream established.

## [2025-10-11]
### Added
- **Core System Import**: Initial commit of 158 files (96,560 lines) from pre-git development environment (Commit b42681).
    - Includes: 
ova/core/ (9 processors), 
ova/brain_regions/ (14 regions), 	ools/ (runtime).

## [2025-06-20]
### Changed
- **Infrastructure**: Migrated development from mobile devices (iOS) to PC environment (Commit d0abad9).

## [2025-05-17]
### Added
- **Project Genesis**: Initial architecture mapping and concept validation on mobile platforms.
