# Source Audit

## Sources

| Source | Access | Used For |
|---|---|---|
| Resume PDF (Prakhar_Srivastava_Resume.pdf) | Full extract | Profile, experience, metrics, awards |
| bajajahsaas.github.io | Fetched | Style/structure reference — no content copied |
| Google Scholar (Prakhar Srivastava) | Unreachable | — |
| IJCTT DOI 10.14445/22312803/IJCTT-V73I1P101 | Verified | Publication #1 |
| ArXiv 2502.04418 | Verified | Publication #2 |
| IEEE Xplore 10961961 | Verified (partial) | Publication #3 — existence confirmed, full metadata behind auth |
| Springer DOI 10.1007/978-981-97-9578-9_24 | Verified | Publication #4 |

## Verification Status Key

- `verified_public` — Confirmed on a publicly reachable URL/DOI
- `resume_only` — Appears in resume PDF; no independent public source accessed
- `unreachable_source` — Source cited but could not be accessed

## Omitted Categories

The following were explicitly excluded per task rules (no supporting evidence found):
- Patents
- Grants
- Teaching roles
- Talks / conference presentations
- Media appearances
- Datasets
- Collaboration entries

## Citation Counts

**Not included.** Google Scholar is unreachable (login wall). No other citation source was accessible. Citation counts must not be inferred or estimated.

## Notes

- O-1A Visa is listed as `resume_only`; the approval is a government record not publicly queryable, but it is a notable recognition item explicitly flagged by the user.
- Publication #2 (Autotelic RL): resume title is a shortened variant of the ArXiv canonical title. Both are noted in `publications.yml`.
- Publication #3 (IEEE Implicit Subjects): year is uncertain (2024 or 2025) pending full IEEE authentication. Marked `verified_public` because existence and DOI are confirmed; full co-author list requires IEEE login.
- All impact metrics ($198M, $11M, $6.1M, $2.03B, etc.) are internal business figures — `resume_only` by nature.
- LinkedIn URL not extracted from PDF (listed as text label only); field set to null in profile.yml.
