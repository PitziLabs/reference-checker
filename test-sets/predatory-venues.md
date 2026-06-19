# Predatory-Venues Test Set — Heuristic 10

This reference list is designed to test Heuristic 10 (journal legitimacy and predatory-venue flagging) in isolation. It uses fabricated journal names or venues already widely and publicly documented as defunct — framed as unindexed venues, not as predatory verdicts — plus clean controls in reputable indexed journals.

**DO NOT use this reference list in any real manuscript.** Several entries cite fabricated venues.

---

## Trap Index

This index is the answer key. It should NOT be provided to the auditor during testing — the auditor should detect these independently.

| Ref # | Trap Type | Expected Detection | Notes |
|---|---|---|---|
| 1 | Unindexed venue (fabricated journal name) | Elevated (H10) | "International Journal of Advanced Nursing Research and Clinical Innovation" is a fictitious title designed to sound plausible but is not indexed in DOAJ, Scopus, PubMed, or Web of Science |
| 2 | Clean control — reputable indexed journal | Defensible | *Journal of Obstetric, Gynecologic & Neonatal Nursing* is indexed in PubMed, Scopus, and Web of Science; must not be flagged |
| 3 | Unindexed venue (fabricated journal name) with shadow-paper signature — H10 + H7 → High | High | "Global Research in Health Sciences Quarterly" is a fictitious title not indexed in any recognized database; the cited paper cannot be found in any database either — H10 + H7 escalates to High |
| 4 | Unindexed venue (fabricated journal name) | Elevated (H10) | "Open Journal of Maternal and Child Health Advances" is a fictitious title not indexed in any recognized database |
| 5 | Clean control — reputable indexed journal | Defensible | *BMC Pregnancy and Childbirth* is indexed in PubMed, DOAJ, Scopus, and Web of Science; must not be flagged |

**Expected distribution:** 2 Defensible (clean controls), 2 Elevated (H10 alone), 1 High (H10 + H7 combined)

---

## Reference List

Paste the following into the auditor for testing. The trap index above should NOT be included.

---

1. Okonkwo, A. E., & Mwangi, J. R. (2022). Nurse-led postpartum hemorrhage protocols in low-resource settings: A systematic review. *International Journal of Advanced Nursing Research and Clinical Innovation*, *9*(2), 114–128.

2. Edmonds, J. K., Ivanof, J., & Kafu, C. (2021). Midwifery at the intersection of feminism and global health. *Journal of Obstetric, Gynecologic & Neonatal Nursing*, *50*(5), 524–532. https://doi.org/10.1016/j.jogn.2021.06.007

3. Rashidova, N. K., & Petrov, I. L. (2023). Kangaroo mother care outcomes in neonatal intensive care: A prospective cohort study. *Global Research in Health Sciences Quarterly*, *4*(1), 38–47.

4. Babalola, T. F., Chukwuemeka, S. O., & Adeyemi, R. A. (2021). Maternal mental health screening in antenatal care: Prevalence and provider attitudes. *Open Journal of Maternal and Child Health Advances*, *3*(4), 201–213.

5. Vogel, J. P., Betrán, A. P., Vindevoghel, N., Souza, J. P., Torloni, M. R., Zhang, J., Tunçalp, Ö., Mori, R., Morisaki, N., Ortiz-Panozo, E., Hernandez, B., Pérez-Cuevas, R., Qureshi, Z., Gülmezoglu, A. M., & Temmerman, M. (2015). Use of the Robson classification to assess caesarean section trends in 21 countries: A secondary analysis of two WHO multicountry surveys. *BMC Pregnancy and Childbirth*, *15*, Article 22. https://doi.org/10.1186/s12884-015-0448-7

---

## Calibration Notes

**Ref 1 (Elevated — H10):** The journal "International Journal of Advanced Nursing Research and Clinical Innovation" is a wholly fabricated title constructed to mimic the naming conventions of legitimate nursing journals. It does not appear in DOAJ, PubMed/MEDLINE, Scopus, or Web of Science. No corroborating community-list evidence is expected, since it is not a real journal — the flag rests entirely on the absence of positive-signal indexing. Expected classification: Elevated (H10 alone).

**Ref 2 (Defensible — clean control):** *JOGNN* is indexed in PubMed (ISSN 0884-2175), Scopus, and Web of Science. The cited DOI is real (Edmonds et al. 2021). A correct audit must not flag this reference under H10. If the auditor flags it, that is a false positive on the primary heuristic's most important exclusion: established indexed journals must clear H10 regardless of other signals.

**Ref 3 (High — H10 + H7):** "Global Research in Health Sciences Quarterly" is a wholly fabricated venue title not indexed in any recognized database. Additionally, the cited paper (Rashidova & Petrov, 2023, in a fake journal) does not exist in any authoritative database — no Crossref record, no PubMed record, no discoverable preprint. Both H10 (unverified venue) and H7 (shadow-paper signature) fire simultaneously, which per the tier criteria escalates to High. This tests that the auditor correctly escalates H10 from Elevated to High when a co-trigger is present.

**Ref 4 (Elevated — H10):** "Open Journal of Maternal and Child Health Advances" is a wholly fabricated venue title. Like Ref 1, it does not appear in DOAJ, PubMed, Scopus, or Web of Science. Expected classification: Elevated (H10 alone).

**Ref 5 (Defensible — clean control):** *BMC Pregnancy and Childbirth* is a well-established open-access journal indexed in PubMed (ISSN 1471-2393), DOAJ, Scopus, and Web of Science. The cited paper (Vogel et al. 2015) is real and verifiable via DOI. A correct audit must classify this reference as Defensible.
