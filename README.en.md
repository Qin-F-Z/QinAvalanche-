<!--
  Copyright (C) 2026  Qin + Chen

  This program is free software; you can redistribute it and/or modify
  it under the terms of the GNU General Public License as published by
  the Free Software Foundation; either version 2 of the License, or
  (at your option) any later version.

  This program is distributed in the hope that it will be useful,
  but WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  GNU General Public License for more details.

  You should have received a copy of the GNU General Public License along
  with this program; if not, write to the Free Software Foundation, Inc.,
  51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
-->

# QinAvalanche Guard v1.0.0

**Open Source · GPL v2.0 · Deterministic Critical-Event Verifiable Computation Laboratory**

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](LICENSE)
[![CLA: DCO-style Signed-off-by](https://img.shields.io/badge/CLA-DCO%20Signed--off--by-blue.svg)](CLA.md)
[![Offline: Zero runtime deps](https://img.shields.io/badge/Offline-Zero%20runtime%20deps-4CAF7A.svg)](QinAvalanche_Guard_互动演示.html)
[![Deterministic: SHA-256 bound](https://img.shields.io/badge/Deterministic-SHA--256%20event%20hash-purple.svg)](#evidence-chain--replayability)

---

## What is this?

QinAvalanche Guard is an **offline, double-click-to-run HTML5 interactive Flash** that demonstrates best practices for sandpile avalanche (BTW Bak–Tang–Wiesenfeld self-organized criticality) modeling:

- **Verifiable computation of deterministic critical events** — every sand drop is bound by a SHA-256 hash chain; third parties can independently replay
- **Counterfactual risk mapping** — runs full integer simulations for every possible drop location on the current state, outputting a global risk heatmap
- **Visual diagnostic laboratory** — integer state view, AI visual baseline (clearly marked as pending blind-test diagnostic baseline), responsive desktop/mobile UI

> **Important Notice**:This software's outputs are for research, education, demonstration, and internal evaluation only. 

---

## License Overview — GNU GPL v2.0

This software is released under the **GNU General Public License v2.0** (OSI/FSF approved open-source license):

| Usage Scenario | Permitted? | Clause Basis |
|---|---|---|
| Internal use | ✅ Free forever | §0 / §1 |
| Non-commercial use (research, education, demo) | ✅ Free forever | §1 |
| Commercial use / SaaS / Embedded distribution | ✅ Free forever, **but MUST be open-sourced** | §2(b) + §3 |
| Modification (Derivative Work) | ✅ Allowed | §2 |
| **Redistributing modified versions** | ✅ **MUST use GPL v2 similarly + provide source code** | §2(b) / §3(a–c) |
| **Sublicensing / Closed-source** | ❌ Forbidden | §4 (no sublicense; violation triggers automatic termination) |
| Patent rights | ⚠️ Bound by §7 — no patent-based restriction of distribution rights | §7 |

### Core GPL v2 Obligations Summary

If you **distribute** (free or paid) modified versions of this software or works that include this software, you **MUST simultaneously**:

1. **License the entire derivative work under GPL v2 identically** (§2b — copyleft virality);
2. **Provide complete source code** or a valid 3-year written offer (§3a/3b);
3. **Keep copyright notices + license notices** intact (§1);
4. **Modified files MUST carry modification date declarations** (§2a).

Internal-only use (without distribution) does not trigger the above obligations.

- **Full GPL v2 license text**: [LICENSE](LICENSE)
- **Disclaimer (required reading)**: [DISCLAIMER.md](DISCLAIMER.md)
- **Contributor DCO-style signing rules**: [CLA.md](CLA.md)
- **Contributing guidelines**: [CONTRIBUTING.md](CONTRIBUTING.md)

---

## Quick Start — Zero Installation, Double-Click to Run

```bash
# Method 1: Double-click
Directly double-click:  QinAvalanche_Guard_互动演示.html

# Method 2: Launch batch (Windows)
Double-click:  启动QinAvalanche_Guard.bat

# Method 3: Command line (Node.js self-test)
node tests/avalanche-kernel-selftest.js
```

**Zero servers, zero accounts, zero network connection**. Recommended browsers: latest Microsoft Edge or Google Chrome.

---

## Core Features

### 1. Integer State (Strict BTW Rules)
- **Black / Green / Purple / Yellow** strictly represent heights 0, 1, 2, 3
- **White flashes** indicate lattice sites that underwent relaxation in this wave
- Open boundary conditions (sand grains dissipate when crossing top/bottom/left/right edges)

### 2. Exact Counterfactual Risk Heatmap
Runs a complete integer simulation for **every possible drop location** on the current state, outputting a global risk heatmap for the next sand drop.

> Per-drop-location genuine simulation, not an AI guess.

### 3. Automated Experiments (Fixed Seed = Reproducible)
- Uses a fixed seed to select drop locations and accumulate successive events
- Same seed across runs → identical event sequence → identical avalanche sizes

### 4. AI Visual Baseline (Pending Blind-Test Diagnostic Baseline)
- Features: global criticality ratio + local color texture + drop height + boundary distance
- Algorithm: historical events as nearest-neighbor estimates
- **Explicitly labeled**: the interface clearly marks it as "pending blind-test diagnostic baseline." **Prediction capability claims MUST only be made after independent train/validation splits, blind testing, and controlled experiments.**

### 5. Evidence Chain & Replayability
- Each event binds: `RULE_VERSION_TAG` + initial-state hash + drop action + result statistics + final-state hash + event hash
- Exportable as `QinEvidence JSON`
- The last event can be replayed with **identical initial state and action**, and event hashes compared → proving determinism

### 6. Responsive Interface
- Desktop: Full 1440 × 1200 layout
- Mobile: Narrow 430 × 1600 adaptive layout

---

## Verification Report

Local verification (Node.js 24 + Microsoft Edge Headless) — ALL PASSED:

- JavaScript syntax check: Passed
- SHA-256 standard known vector `abc`: Passed
- 3×3 center single-relaxation topology: Passed
- **Mass conservation**: `initial mass + 1 = final mass + boundary dissipation`: Passed
- Deterministic replay with identical initial state & action: Passed
- Real browser interaction: sand-drop event completes; avalanche size, event hash, replay, and evidence export all correct
- Analysis view toggle: Integer state → AI visual baseline: Passed
- **Offline requirement**: Running code invokes zero remote endpoints, uploads zero experiment data: Passed
- Desktop + narrow-screen rendering: Passed

> Full verification report: [VERIFICATION_REPORT.md](VERIFICATION_REPORT.md)
> SHA-256 delivery checksums: [SHA256SUMS.txt](SHA256SUMS.txt)
>
> ⚠️ Local verification ≠ third-party independent audit ≠ scientific/safety certification. See [DISCLAIMER.md §1.2](DISCLAIMER.md).

---

## Repository Structure

```
QinAvalanche/
├── QinAvalanche_Guard_互动演示.html    Complete offline app (contains all runtime code)
├── 启动QinAvalanche_Guard.bat         Windows launch entry
├── source/
│   └── qin-avalanche-lab.fragment.html  Source fragment embeddable in product platforms
├── tests/
│   └── avalanche-kernel-selftest.js     Core conservation/determinism/SHA-256 self-test
│
├── QinAvalanche_Guard_产品定位与科学边界.md
│
├── preview-desktop.png / preview-mobile.png
├── SHA256SUMS.txt
├── VERIFICATION_REPORT.md
├── README.original.md                   Original internal delivery notes archive
├── README.md                            Chinese readme (main)
├── README.en.md                         English readme (this file)
│
├── LICENSE                                 【GNU GPL v2 full text】
├── CLA.md                                  【DCO attribution contribution rules】
├── DISCLAIMER.md                           【Disclaimer + third-party acknowledgments】
├── CONTRIBUTING.md                         【Contributing guidelines】
├── .gitignore                              Git ignore rules
└── CITATION.cff                            Academic citation format
```

---

## Scientific Boundary Statements (Required Reading)

> Full statement in [QinAvalanche_Guard_产品定位与科学边界.md](QinAvalanche_Guard_产品定位与科学边界.md) and [DISCLAIMER.md](DISCLAIMER.md).

- "Exact counterfactual" means **genuine simulation per drop location**, not an AI guess.
- "Replay" proves **identical inputs produce identical outputs in this deterministic kernel**; it does NOT equal prediction of unknown real systems.
- "AI visual baseline" MUST undergo independent training/validation splits, blind testing, and controlled experiments before prediction capability can be claimed.
- Sandpile model results **MUST NOT be directly extrapolated** to materials, geology, finance, or other real-world systems.
- **MUST NOT be used in safety-critical systems, civil engineering design, geological hazard forecasting, financial risk models, medical clinics, regulatory compliance, or any scenario requiring certification or auditing.**

---

## Copyright & License Header Standard (GPL v2 Compliant)

Every source code file MUST begin with the standard GPL v2 recommended declaration (syntax adapted to file type).

**JavaScript / Python / Shell types:**

```javascript
/*
 *  QinAvalanche Guard — Sandpile Avalanche Deterministic Critical-Event Computation Lab
 *  Copyright (C) 2026  Qin + Chen
 *
 *  This program is free software; you can redistribute it and/or modify
 *  it under the terms of the GNU General Public License as published by
 *  the Free Software Foundation; either version 2 of the License, or
 *  (at your option) any later version.
 *
 *  This program is distributed in the hope that it will be useful,
 *  but WITHOUT ANY WARRANTY; without even the implied warranty of
 *  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 *  GNU General Public License for more details.
 *
 *  You should have received a copy of the GNU General Public License along
 *  with this program; if not, write to the Free Software Foundation, Inc.,
 *  51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
 */
```

**HTML / Markdown types:**

```html
<!--
  QinAvalanche Guard — ...
  Copyright (C) 2026  Qin + Chen
  License: GNU GPL v2.  See LICENSE file for full terms.
-->
```

**Batch .bat / .txt comment types:**
```bat
@REM  Copyright (C) 2026  Qin + Chen
@REM  License: GNU GPL v2.  See LICENSE file for full terms.
```

---

## Version Information

- Product name: QinAvalanche Guard
- Evidence framework: QinEvidence
- Version: v1.0.0
- Initial release date: 2026-08-09
- Open-source release date: 2026-09-02
- **License**: GNU General Public License **v2** (or any later version, at your option)

---

## Contact & Contributing

- **Issues / PRs**: GitHub repository Issues / Pull Requests
- **Contribution CLA**: DCO-style signing required <your.email@example.com> two-line signature at the end of commit message; see [CLA.md](CLA.md))
- **Security disclosure (non-public)**: See [CONTRIBUTING.md §10](CONTRIBUTING.md)

---

*QinAvalanche Guard is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2, or (at your option) any later version. QinAvalanche Guard is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. A copy of the license is in the [LICENSE](LICENSE) file.*
