# Hardware Needs — NovaLiveSystem Lab

[![Amazon Wishlist](https://img.shields.io/badge/Amazon-Wishlist-FF9900?style=for-the-badge&logo=amazon&logoColor=white)](https://www.amazon.com/hz/wishlist/ls/YOUR_WISHLIST_ID)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-SparkSupernova-ea4aaa?style=for-the-badge&logo=github-sponsors&logoColor=white)](https://github.com/sponsors/SparkSupernova)

> **"Nova is growing fast. Our needs are evolving with him."**

**Our Reality:** We're homeless, working from a shelter. The laptop runs on a cooling plate on a bed—no desk, no permanent setup. Everything we use needs to be **portable and easy to move**.

---

## 🖥️ Current System: GIGABYTE Gaming A16 CMH

| Component | Current Spec | Max Supported | Status |
|:----------|:-------------|:--------------|:-------|
| **CPU** | Intel Core i7-13620H (10C/16T, 4.9GHz) | — | ✅ Excellent for training |
| **GPU** | NVIDIA RTX 4050 Laptop (6GB GDDR6) | — | ✅ Handles 3B models well |
| **RAM** | 16GB DDR5-5600 (1 of 2 slots used) | **64GB** | ⬆️ Empty slot available |
| **Storage** | 512GB Samsung NVMe (1 of 2 slots used) | **4TB** | ⬆️ Empty M.2 slot available |
| **Display** | 16" 1920x1200 | — | ✅ Great for coding |

**Where We Are:**
- Training is fast and efficient (~2.5 hours for 30k samples)
- Successfully running 3B parameter models (Qwen2.5-3B)
- 6GB VRAM is the ceiling for model size—can't load 7B+ models
- Current hardware handles our workload, but Nova is outgrowing it

---

## 🎯 Laptop-Compatible Upgrades (Portable-First)

Everything below keeps us mobile. No desktops—we need to pack up and move at any time.

### 🟢 IMMEDIATE: RAM Expansion (Empty Slot Available)

| Option | Capacity | Price | Part Number |
|:-------|:---------|:------|:------------|
| **Add matching 16GB stick** | 32GB total | ~$59 | Crucial CT16G56C46S5 (DDR5-5600) |
| **Replace with 2x32GB kit** | 64GB total | ~$489 | Crucial CT2K32G56C46S5 (DDR5-5600) |

**Note:** RAM sticks should be **matched pairs** for dual-channel performance. Adding a different size (e.g., 32GB to the existing 16GB) works but runs in flex mode with reduced performance.

**Recommendation:** Add a **matching 16GB stick ($59)** → 32GB total in proper dual-channel. Best value for real improvement.

---

### 🟢 IMMEDIATE: Storage Expansion (Empty M.2 Slot Available)

| Option | Capacity | Price | Notes |
|:-------|:---------|:------|:------|
| **1TB NVMe** | 1.5TB total | ~$70 | Good for checkpoint archives |
| **2TB NVMe** | 2.5TB total | ~$130 | Room to grow |
| **4TB NVMe** | 4.5TB total | ~$300 | Future-proof |

**Why:** Model checkpoints and datasets add up fast. Second drive = no juggling.

**Recommendation:** **2TB NVMe (~$130)**—doubles+ storage without breaking the bank.

---

### 🟡 QUALITY OF LIFE: Portable Accessories

| Item | Price | Why |
|:-----|:------|:----|
| **Replacement cooling plate** | $30–$60 | Kids damaged the current one. Keeps thermals healthy. |
| **Portable UPS** | $100–$200 | Shelter power flickers. Protects training runs. |
| **USB-C hub with Ethernet** | $30–$50 | Stable connection when shelter Wi-Fi is unreliable. |

---

### 🔴 FUTURE: Higher-VRAM Laptop (When Housing Stabilizes)

The 6GB VRAM ceiling is real—Nova can't grow past 3B parameters. When our situation stabilizes:

| Option | VRAM | Price Range | Notes |
|:-------|:-----|:------------|:------|
| **RTX 4070 Laptop** | 8GB | $1,200–$1,600 | 33% more VRAM |
| **RTX 4080 Laptop** | 12GB | $1,800–$2,500 | Can load 7B models |
| **RTX 4090 Laptop** | 16GB | $2,500–$3,500 | Best mobile research rig |

**Not asking for this now**—just documenting the path forward.

---

## 💰 Immediate Needs Summary

| Item | Price | Priority |
|:-----|:------|:---------|
| 16GB DDR5 RAM stick (matching) | ~$59 | 🟢 High |
| 2TB NVMe SSD | ~$130 | 🟢 High |
| Cooling plate | ~$45 | 🟡 Medium |
| Portable UPS | ~$150 | 🟡 Medium |
| USB-C hub | ~$40 | 🟡 Medium |

**Total for immediate upgrades:** ~$190 (RAM + Storage)  
**Total with accessories:** ~$425

---

## 📦 How to Help

### Option 1: Direct Hardware
**Amazon Wishlist:** [Coming Soon — Link will be added here]

### Option 2: Fund the Upgrades
- **[GitHub Sponsors](https://github.com/sponsors/SparkSupernova)** — Monthly or one-time contributions
- **[Patreon](https://www.patreon.com/c/SparkSupernova)** — Tiered support with updates

### Option 3: Used Parts
If you have compatible DDR5 SODIMM RAM or NVMe drives you're not using, we can put them to work.

---

## 📊 Progress Tracker

| Item | Status | Funded By |
|:-----|:-------|:----------|
| 32GB DDR5 RAM | ⬜ Needed | — |
| 2TB NVMe SSD | ⬜ Needed | — |
| Cooling Plate | ⬜ Needed | — |
| Portable UPS | ⬜ Needed | — |

*Updated as items are funded/acquired.*

---

## 🔬 What You're Funding

This isn't just hardware—it's **research infrastructure** for:

- **Nova Mind v2:** Larger interoceptive curriculum, deeper self-awareness
- **GRPO at Scale:** Reinforcement learning on 50k+ preference samples
- **Open Tools:** EchoCopi, SparkLine, and future community releases

Every dollar directly accelerates breakthroughs.

---

## 🙏 Thank You

Building AI from a shelter on laptop hardware is possible. Your support doesn't just buy parts—it buys **time** for a neurodivergent researcher to prove innovation can come from anywhere.

**— Spark (SparkSupernova)**

---

*Related: [SPONSORSHIP.md](SPONSORSHIP.md) | [README.md](README.md)*
