<!--
Copyright (c) 2026 JG Systems Consulting Ltd. MIT License (see ../LICENSE).
SPDX-License-Identifier: MIT
-->

# Cross-pack boundaries

UK defence publication has one content owner, this repo, once that publication is vetted and packaged. SE and nuclear do not carry that publication as a content pack. Topic-name overlap is allowed. Source-document overlap is not. A sibling may name the canonical slug and repo. A sibling must not install a same-slug content copy.

| Topic | uk-defence owns | SE may keep | Nuclear may keep | Must not |
|---|---|---|---|---|
| Safety cases | JSP 815 Element 4; JSP 376 once moved | Safety-case method from sources other than those JSPs | NRC practice already in the nuclear repo | A second content pack of JSP 815 or JSP 376 |
| Assurance | JSP 815 Element 12, Annex H, and Annex G if folded in | Assurance method from other sources | No JSP text | A second content pack of JSP 815 |
| Risk | JSP 815 Element 4 defence risk vocabulary; JSP 376 once moved | Risk method from other sources | No JSP text | A second content pack of those JSPs |
| HFI | JSP 912 once moved | HFI sources that are not JSP 912 | No JSP 912 text | A content copy of JSP 912 |
| AI safety | JSP 936 once moved | AI or systems-engineering sources that are not JSP 936 | No JSP 936 text | A content copy of JSP 936 |
| Software assurance | A UK defence source only after step 1. DEF-STAN 00-051 is the candidate and its title is unconfirmed | SE signposts for excluded avionics standards; no DEF-STAN text | No DEF-STAN text | DEF-STAN chapters before a recorded cover licence |

ISO 45001 text is excluded in every sector and signposted only here (`iso-45001-signpost`). JSP 814 and DEF-STAN 00-970 are not given a pack in this pass. The nuclear repo was not edited because the 2026-11-22 fleet survey found no UK defence content there.
