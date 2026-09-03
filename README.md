<!--
  isual baseline: Passed
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
