# Contributor License / Developer Certificate of Origin (DCO)
# QinAvalanche Guard — Contribution Sign-off Rules

This Project is licensed under the **GNU General Public License, version 2**
(GPL-2.0-only / GPL-2.0-or-later; see the file `LICENSE`). To keep the
provenance of every contribution clean and legally defensible for every
downstream user under copyleft, every contributor MUST certify the
following DCO-style statement for every submission.

==============================================================================
                 CONTRIBUTOR CERTIFICATION OF ORIGIN
                     (Developer Certificate of Origin 1.1)
==============================================================================

By making a contribution to this project, I certify that:

  (a) The contribution was created in whole or in part by me and I
      have the right to submit it under the GNU General Public License
      version 2 (the "License"); or

  (b) The contribution is based upon previous work that, to the best of
      my knowledge, is covered under an appropriate open source license
      and I have the right under that license to submit that work with
      modifications, whether created in whole or in part by me, under
      the License (GNU General Public License, version 2, or any later
      version published by the FSF at my option); or

  (c) The contribution was provided directly to me by some other person
      who certified (a), (b) or (c) and I have not modified it.

  (d) I understand and agree that this project and the contribution are
      public and that a record of the contribution (including all
      personal information I submit with it, including my sign-off) is
      maintained indefinitely and may be redistributed consistent with
      this project or the open source license(s) involved.

  (e) I am legally competent to enter into this certification. If my
      contribution was created in the course of my employment, as a
      work for hire, or in connection with work performed for a third
      party, I certify that I have received all necessary releases,
      permissions, waivers, and consents from the third party (including
      my employer) to submit the contribution under the terms of this
      certification and of the GNU General Public License, version 2.

==============================================================================
                          HOW TO SIGN OFF
==============================================================================

To accept and sign the above Certification for a specific contribution,
you MUST include the following two lines at the END of the commit
message of every commit that you submit:

       Signed-off-by: Your Full Name <your.email@example.com>
       License: GPL-2.0-or-later

Example:

    commit 3af2c9b...
    Author: Ada Lovelace <ada@analytical.engine>
    Date:   Wed Jul 15 12:00:00 1843 +0000

        fix: preserve sand conservation at open-boundary corners

        The integer kernel in relax_step() was under-counting the
        boundary-loss accumulator for corner cells (0,0 / 0,N-1 /
        N-1,0 / N-1,N-1) when two neighbors both relaxed.

        Fixes #17.

        Signed-off-by: Ada Lovelace <ada@analytical.engine>
        License: GPL-2.0-or-later

If you forget on the last commit, you can amend:

    git commit --amend -s
    # or manually append the two lines to the commit message

You may optionally also append the standard `GPL v2 boilerplate`
notice to new source files (see README.md § "License Headers" for
the canonical text per file type).

==============================================================================
                     REJECTION OF INVALID SIGN-OFFS
==============================================================================

A contribution will NOT be merged if:

  1. It lacks the required `Signed-off-by` trailer; OR

  2. The `Signed-off-by` trailer does not match a real, deliverable
     email address of the person named in the `Author:` field
     (reasonable aliases are accepted); OR

  3. The contribution contains material that the reviewer has
     reasonable grounds to believe was copied, adapted, or derived
     from a third-party work that is not either:
        (i)  in the public domain;
        (ii) available under GPL-2.0-or-later OR under a license
             explicitly listed as GPLv2-compatible by the Free
             Software Foundation at
             https://www.gnu.org/licenses/license-list.en.html;
        (iii)accompanied at the time of submission by a clear
             written statement of the source license, copyright
             notice, and upstream URL.

  4. The contributor is unwilling or unable to cure any of (1)–(3)
     in a reasonable time.

No legal or technical advice is provided by the project maintainers
through any merge decision. Every contributor remains solely
responsible for their own submissions and for verifying the license
compatibility of any incorporated third-party material.

==============================================================================
                               EMPLOYER NOTICE
==============================================================================

If you are contributing as an employee, contractor, or agent of a
company, university, government agency, or other legal entity, and
the contribution was created in the course of such employment or
contract, it is YOUR RESPONSIBILITY to ensure that you have full
written authority to submit the contribution under the GNU GPL v2
and under this DCO certification. If in doubt, do not submit until
you have received written authorization from the appropriate person
at your organization.

The Project may, at its sole discretion, require additional
written confirmation (e.g., an employer disclaimer email or a
signed corporate CLA) before merging contributions that appear to
be works made for hire. A standard template employer disclaimer is
shown below for reference only; use of this exact template is NOT
required, but the essential points must be present.

      -------- Employer Disclaimer Template (Optional) --------
      [Company / University Name], hereby disclaims all copyright
      interest in the Program contribution <commit hash / PR title>
      made by <Employee Name>.

      <signature / name of authorized signatory>, <title>
      <date>
      ---------------------------------------------------------

==============================================================================
                               DATA PRIVACY
==============================================================================

By submitting a contribution, you acknowledge and agree that a
permanent public record of the submission (including your name,
email address, pseudonym, GitHub username, and commit message) will
be retained in the repository's git history, may be mirrored or
forked by third parties, and may be redistributed under the terms
of the GNU General Public License version 2 or later. You consent
to such retention and redistribution, and understand that public
git history is effectively irreversible — requests for removal of
personal data will be processed to the extent required by law but
cannot be guaranteed for every third-party mirror.

==============================================================================
                  END OF DCO / CONTRIBUTION CERTIFICATION
==============================================================================
