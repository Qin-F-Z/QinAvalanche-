# DISCLAIMER, LIMITATIONS AND THIRD-PARTY ACKNOWLEDGEMENTS
# QinAvalanche Guard Project

This document supplements the LICENSE file, the CLA file, and the
README. It contains specific disclaimers and lists third-party
works and technologies that this Project relies on or is built
upon. All capitalized terms not defined here have the meanings
given in the GNU General Public License, version 2 (the "License").

==============================================================================
                           PART 1 — DISCLAIMERS
==============================================================================

Please read the following carefully before using or distributing
the Software. These disclaimers are incorporated by reference into
the "NO WARRANTY" section (§11–12) of the GNU GPL v2 under which
this Software is offered. The scope and intent of this Part 1 is
to elaborate, in non-legalese, on the kinds of use that are
expressly NOT warranted and that the authors specifically
disclaim, as permitted by the first sentence of §11 ("EXCEPT WHEN
OTHERWISE STATED IN WRITING"). Nothing in this document expands
or diminishes the disclaimers of warranty in the License itself
beyond what the License permits by way of written elaboration.

------------------------------------------------------------------------------
                    1.1  NO SCIENTIFIC OR ENGINEERING CERTIFICATION
------------------------------------------------------------------------------

QinAvalanche Guard ("the Program") is an educational, research, and
visualization tool that implements a discrete cellular-automaton
model known as the Bak–Tang–Wiesenfeld (BTW) sandpile model. It is
NOT certified, audited, or validated for any real-world
safety-critical, regulatory, or engineering use.

SPECIFICALLY, AND WITHOUT LIMITING THE "NO WARRANTY" CLAUSE IN THE
PROJECT LICENSE, YOU UNDERSTAND AND AGREE THAT:

(a) The deterministic sandpile kernel, the "counterfactual risk
    heat-maps", the "AI visual baseline", the statistical
    distributions, the power-law fits, the hash chains, and every
    other output produced by the Program are outputs of a
    mathematical model only. They are not and must not be taken as
    predictions of real events in the physical world.

(b) The results of the Program, even if statistically consistent
    with published observations on a chosen dataset, DO NOT
    constitute evidence of any predictive, diagnostic, or prognostic
    power regarding:

        - 土木工程 / civil and structural engineering design;
        - 结构力学 / structural mechanical load analysis;
        - 地质灾害预报 / geological hazard forecasting
              (landslides, earthquakes, volcanic activity, etc.);
        - 气象或气候风险 / meteorological or climate-risk models;
        - 材料疲劳 / material fatigue or structural degradation;
        - 金融风险 / financial risk, VaR, stress-testing,
              algorithmic trading, or investment models;
        - 能源或电网稳定性 / power grid or energy grid stability;
        - 医疗或临床 / medical or clinical use cases;
        - 任何需要经过监管合规、第三方审计或法律责任的场合
              / any regulated, audited, or legally liable scenario.

(c) Any analogy drawn between the output of the Program and any
    real physical, economic, or social system is provided solely
    for research discussion and educational purposes. Extrapolation
    of results beyond the deterministic, integer-based kernel of
    the Program is ENTIRELY AT YOUR OWN RISK.

(d) The "复演" (replay / re-enactment) feature of the Program
    proves only the deterministic repeatability of the Program's
    own kernel with identical input. It does NOT prove anything
    about the correspondence between the Program model and the
    real world.

------------------------------------------------------------------------------
                    1.2  NO THIRD-PARTY AUDIT
------------------------------------------------------------------------------

The file VERIFICATION_REPORT.md included in this repository, and
any in-house verification runs described in the SHA256SUMS.txt,
were produced by the upstream authors as a reproducibility aid
for the user. They are NOT:

    - a third-party independent security or correctness audit;
    - a formal certification of any kind (ISO, IEC, CMMI, TÜV, etc.);
    - a scientific peer review;
    - a regulatory compliance statement.

Any claim to the contrary should be rejected. Before relying on
the Program's output for non-educational purposes, you must
commission or perform your own independent verification by
qualified and disinterested third parties.

------------------------------------------------------------------------------
                    1.3  HASH AND EVIDENCE CHAIN LIMITATIONS
------------------------------------------------------------------------------

The "QinEvidence" JSON export feature, the SHA-256 event hashes,
the op-log chain, and the state-hash bindings are designed to
protect against ACCIDENTAL or ADVERSARIAL TAMPERING WITHIN THE
PROGRAM'S OWN KERNEL. They do NOT:

    - guarantee the correctness of the deterministic kernel itself
      (correctness is a separate mathematical property that must be
      verified by formal methods, peer review, or your own audit);
    - protect against hardware failures, supply-chain attacks,
      firmware rootkits, hypervisor vulnerabilities, or any
      attacks that execute with privilege above the user process;
    - bind against out-of-band changes to the underlying platform,
      browser, or JavaScript runtime;
    - constitute a digital signature in any legally recognized
      sense (no PKI / X.509 / GPG trust model is used unless
      separately configured by the user).

------------------------------------------------------------------------------
                    1.4  AI VISUAL BASELINE DISCLAIMER
------------------------------------------------------------------------------

The feature labelled "AI Visual Baseline" or "AI 视觉基线" in the
Program is a deterministic nearest-neighbor estimator based on
hand-crafted features. It is NOT:

    - a machine-learning model trained on an external dataset
      split with proper train/validation/test separation;
    - a statistically validated predictor;
    - a benchmarked diagnosis tool.

The Program UI explicitly marks this feature as a "待盲测诊断
基线" ("baseline pending blind validation"). It must not be used
as a component of any diagnosis, recommendation, or decision
system.

------------------------------------------------------------------------------
                    1.5  NO FINANCIAL, LEGAL, OR MEDICAL ADVICE
------------------------------------------------------------------------------

The Program is not intended to provide, and does not constitute,
financial advice, investment advice, legal advice, tax advice,
medical advice, or any other form of professional advice. All
decisions made on the basis of the Program output, whether in
business, finance, engineering, research, or personal matters,
are Your sole responsibility.

------------------------------------------------------------------------------
                    1.6  NO COPILEFT EVASION
------------------------------------------------------------------------------

If you distribute the Program or a work based on the Program in
any form (source, binary, SaaS service, embedded component,
hardware peripheral, or any medium of communication), you are
bound by §2(b) and §3 of the GNU GPL v2 and must:

    (i)   license the work as a whole at no charge to all third
          parties under the terms of the GNU GPL v2; AND
    (ii)  provide (or offer to provide) complete corresponding
          machine-readable source code as required by §3.

Distributing the Program under additional or more restrictive
terms (for example, a proprietary EULA or a license that forbids
re-distribution) WITHOUT also complying with the GNU GPL v2 is a
material breach of the License and, per §4, automatically
terminates your rights under the License.

==============================================================================
                         PART 2 — THIRD-PARTY ACKNOWLEDGEMENTS
==============================================================================

This Project does not bundle or require any mandatory third-party
runtime dependency for the interactive HTML version of QinAvalanche
Guard. The entire kernel runs as vanilla ECMAScript inside the
browser. No network call, CDN load, or remote dependency is
required at runtime.

Nevertheless, portions of the Program or the development
toolchain make reference to, build upon, or are influenced by the
following public works. We gratefully acknowledge their authors
and contributors.

------------------------------------------------------------------------------
                    2.1  COMPUTER-SCIENCE FOUNDATIONS
------------------------------------------------------------------------------

(a) Bak–Tang–Wiesenfeld (BTW) Sandpile Model
    Reference: P. Bak, C. Tang, K. Wiesenfeld, "Self-organized
               criticality: An explanation of the 1/f noise,"
               Phys. Rev. Lett. 59, 381–384 (1987).
    License:   Public domain (idea / scientific publication).

(b) SHA-256 Cryptographic Hash (FIPS PUB 180-4)
    Reference: NIST FIPS PUB 180-4, "Secure Hash Standard
               (SHS)", 2015.
    Used by:   The browser's Web Crypto API (crypto.subtle.digest)
               and, in the self-test file tests/avalanche-kernel-selftest.js,
               the Node.js built-in crypto module.
    License:   Public domain (standard).

(c) Int32Array / TypedArray (ECMAScript 2015 / ES6)
    Used by:   The kernel for deterministic state storage.
    License:   ECMA-262, standardized by Ecma International.

------------------------------------------------------------------------------
                    2.2  DEVELOPMENT ENVIRONMENT (NOT BUNDLED)
------------------------------------------------------------------------------

The following tools are used or recommended during Development
but are NOT distributed as part of this Repository. You must
source and accept them separately under their own licenses.

| Tool / Library        | Typical purpose              | License                  |
|-----------------------|------------------------------|--------------------------|
| Node.js (>= 20)       | Running self-test JS         | MIT-style (Node license) |
| Python (>= 3.9)       | Statistical validation       | PSF v2                   |
| NumPy                 | Vector / array math          | BSD-3-Clause             |
| SciPy                 | Statistical distributions    | BSD-3-Clause             |
| Matplotlib            | Plotting                     | PSF-style / BSD-compt.   |
| GitHub Actions (CI)   | Continuous integration       | GitHub ToS / MIT (runs)  |
| VS Code / Edge        | Editing / runtime            | EULA / Microsoft         |

------------------------------------------------------------------------------
                    2.3  OTHER INSPIRATIONS (NO CODE COPIED)
------------------------------------------------------------------------------

The Program's visual design and interaction patterns were
inspired by:

    -  Modern CSS Grid / CSS Variables: W3C Recommendations,
       no code copied.
    -  Color palette conventions: generic dark-green theme used
       in open-source scientific dashboards. Designed in-house;
       no third-party asset embedded.
    -  Iconography and interface metaphors: original in-house
       design; no third-party font, logo, or artwork embedded.

------------------------------------------------------------------------------
                    2.4  BUNDLING STATUS OF EACH REPOSITORY FILE
------------------------------------------------------------------------------

To the best of our knowledge, the following files in this
repository contain NO embedded third-party code other than what
is explicitly listed in Sections 2.1 and 2.2 above:

| File                                         | Third-party code? |
|----------------------------------------------|-------------------|
| QinAvalanche_Guard_互动演示.html              | None (pure HTML/CSS/ES, browser APIs only) |
| source/qin-avalanche-lab.fragment.html        | None              |
| tests/avalanche-kernel-selftest.js            | Node crypto built-in only |
| SHA256SUMS.txt                                | None              |
| VERIFICATION_REPORT.md                        | None              |
| README.md                                     | None              |
| LICENSE (GNU GPL v2)                          | FSF template; verbatim, as permitted |
| CLA / DISCLAIMER / CONTRIBUTING               | Community-authored, templates adapted |

If You discover any material in the repository that You believe
should be acknowledged under a third-party license, please open a
GitHub Issue immediately. The project maintainers will review and
correct the record in good faith, and if necessary produce a
source-release that either complies with the upstream license or
removes the infringing material.

==============================================================================
                   PART 3 — COMPLIANCE WITH THIS DOCUMENT
==============================================================================

Any distribution of the Program, or of a work based on the
Program, must include this DISCLAIMER.md file (or its content,
verbatim, in a user-visible file). All disclaimers in Part 1 must
be reproduced in all copies. All third-party acknowledgements in
Part 2 must be reproduced in source distributions.

Failure to include this DISCLAIMER.md in a source distribution
that you forward to a third party does NOT excuse you from the
NO WARRANTY clauses of the GNU GPL v2; it merely removes one of
the explicit written disclaimers that further amplify them.

==============================================================================
                              END OF DISCLAIMER
==============================================================================
