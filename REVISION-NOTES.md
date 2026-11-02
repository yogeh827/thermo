# Language and style revision — notes

**Document:** `THERMAL BATTERY MANAGEMENT.docx` (unchanged, kept as the original)
**Revised:** `THERMAL BATTERY MANAGEMENT (revised).docx`

27 of 356 paragraphs were revised. Everything else is byte-identical to the original.

---

## 1. Assessment

The paper was already in good shape. The sentence-level prose is clear, the
terminology is consistent, and the arithmetic is sound — I checked it and found no
errors:

- Group sizes (9 + 3 + 4 + 5 + 2 + 2) sum to 25, and "nine studies", "the three
  studies", "the five studies" all match their sections.
- Method counts in §5.2 (10 experimental + 7 numerical + 3 both + 5 not stated) match
  Table 2 exactly.
- "PCM is part of 22 of the 25 systems" is correct; the three exceptions ([15], [16],
  [17]) are the right ones.
- "Twenty-one of the twenty-five appeared in 2021 or later" is correct (four
  pre-2021: [13], [15], [17], [18]).
- Derived percentages check out: 97.5 → 48.9 °C is −49.8% [21]; 51.16 − 40.81 =
  10.35 °C [8]; 55 − 12 = 43 [17]; 13S8P = 104 cells [21].
- Equation (1) matches the standard Bernardi form for *I* positive on discharge, and
  the sign convention agrees with the text that follows it.
- All 25 references are cited in the body; no orphans.

Because of this, I did **not** rewrite prose that was already working. The edits
target three specific problems instead.

## 2. What was changed

**a. Repetitive structure (the main "AI fingerprint" in the document).**
Every one of the 25 study paragraphs opened with "Author et al. [n] + verb", and four
of six subsections closed with a formulaic "These studies show/agree that…". I varied
roughly a third of these so the rhythm breaks up, while keeping the author-first form
as the default, since that is the convention readers expect in a review. Examples:

- §3.2 — five consecutive "X is simple but has weakness Y" sentences recast with
  varied structure.
- §4.1 close — "Taken together, these nine studies show…" → "Across these nine
  studies, PCM–liquid hybrids hold modules…".
- §4.2 close — "The PCM–air studies agree that air cannot replace…" → "In the PCM–air
  studies, neither element can substitute for the other: …".
- §4.3 close — "Heat-pipe hybrids therefore offer strong uniformity, since ΔT
  reductions of 30–77% are reported, and, in the case of [14], the ability to…"
  (broken parallel) → "Uniformity is the clear strength of heat-pipe hybrids, with
  reported ΔT reductions of 30–77%, and the design in [14] adds…".

**b. Genuine errors and awkward constructions.**

| Location | Issue | Change |
|---|---|---|
| Declaration | "The **author** declares" with four registration numbers | "The **authors declare**" |
| §3.3 | "A second family… A third family…" with no first family named | First pairing now named explicitly |
| §4.3 [16] | "coupled L-shaped heat pipes with a cold plate and compared **it**" — unclear antecedent | "compared **the arrangement**" |
| §4.4 [17] | "dropped from 55 °C to 12 °C, **about 43 °C**" — absolute and difference in apposition | "a fall of about 43 K" |
| §3.1 | "Irreversible heat **comes from**… Reversible heat **comes from**…" | "arises from" / "follows from" |
| §4.1.2 [6] | "The PCM plate **brought**… The hybrid **brought**…" | second → "took them to" |
| §4.1.1 [4] | "pack whose cold plates **integrate** PCM" after "**integrating**" | "in which PCM is embedded in the pack-level cold plates" |
| §2.3 | tense shift: "it **was** placed… is placed" in one sentence | both past tense |
| Abstract | "and it proposes directions for future research" tacked onto a long sentence | split into its own sentence |
| §1 | "usable capacity falls" then "reduces the usable capacity" | second → "erodes the capacity of the pack as a whole" |
| §1 | roadmap was one mechanical sentence per section | merged into three sentences |

**c. Two internal inconsistencies.**

1. **Abstract unit clash.** "reductions ranged from about **1 K to about 43 °C**" mixed
   both units inside one range for the same quantity. Now "roughly **1–43 K**", with
   [17] in §4.4 and §5.3 made to agree. For a temperature *difference* 1 K ≡ 1 °C, so
   no value changed. See flag 3 below.
2. **"one of the few" vs "only".** §4.1.1 called [4] "one of the few studies validated
   on a complete, manufactured pack", but §5.2 and §6 both state that *only* [4] does
   this. Aligned to "the only reviewed study validated on a complete, manufactured
   pack". See flag 7.

**Also corrected:** "single cooling method" → "single-mode" (matching the rest of the
paper); "keep the pack uniform" → "keep the pack thermally uniform"; "about 10.35 °C"
("about" + two decimals) → "10.35 °C"; "kept the average temperature within 34 °C" →
"below 34 °C" (matching Table 2's "≤ 34 °C"); §5.2 "This **confirms** that PCM… is the
common building block" → "is **thus** the common building block **across this
sample**", which is what a 25-paper sample supports and is consistent with the
limitations in §2.4. Conclusion (1) was softened from "Hybrid BTMS **consistently
outperform** single-mode systems" to "In every study reviewed, the hybrid system
outperformed the single-mode baseline **against which it was compared**", since §5.1
and §5.3 are explicit that each result is measured against its own baseline.

## 3. What was deliberately left alone

Headings, numbering, both figures, all four captions, Table 1, Table 2, the
abbreviations table, equation (1) with its subscripts, the bold lead-ins in §6 and §7,
and all 25 references including every DOI. No numerical value, finding, or conclusion
was altered.

**Verified after editing:** 356 → 356 paragraphs; 2 → 2 figures; 21 → 21 package
entries; references, captions, equation and tables identical; numerals identical
paragraph-by-paragraph except the one noted in flag 6.

---

## 4. Flags — please check these

**Needs your decision or a look at the sources:**

1. **Registration numbers.** `25BME1219 25BME1261 25BME1297 25BMV1034` — the fourth
   reads **BMV** where the others read **BME**. Possible typo; I did not touch it.
   There is also a trailing space, and no separators between the numbers.
2. **`Tmax` is not subscripted** (5 occurrences) while `U`~ocv~ in equation (1) and its
   definition correctly uses Word subscript formatting. Fixing this means adding
   subscript runs, which risked the equation, so I left it for a manual pass in Word.
   Likewise `Al₂O₃` uses Unicode subscript characters rather than Word formatting —
   consistent enough to read, but mixed under the hood.
3. **°C vs K for temperature differences.** The paper reports differences in °C in some
   places and K in others, mirroring the source papers. I fixed only the one range that
   mixed both units internally (flag in §2c). Harmonising the rest is a defensible
   editorial choice but would mean departing from how each source reported its result —
   your call.
4. **§4.1.1 [1]: "PCM cut temperature by 47%"** — 47% of *what*? A percentage reduction
   in absolute temperature is ambiguous; it is probably the temperature *rise* above
   ambient. Worth checking Hyun et al. and stating the basis.
5. **§4.1.2 [7]: "kept the cells well below 41.2 °C"** — "well below" with a figure to
   one decimal is self-contradictory. I changed it to "held the cells below 41.2 °C",
   but please confirm whether 41.2 °C was the measured maximum (in which case "reached
   a maximum of 41.2 °C" would be more accurate).
6. **§4.3 [14]: "brought the internal temperature difference close to 0 °C"** — a
   difference stated in °C reads oddly. Changed to "closed the internal temperature
   difference to near zero". This is the only place a numeral ("0") was removed.
7. **§4.1.1 [4]: "one of the few" → "the only".** Please confirm [4] really is the only
   full-pack validation in your set, since §5.2 and §6 already assert this.
8. **Table 2 names "Layout D" for [1]**, but the prose only says "the best layout". I
   left the prose as-is; consider naming the layout for consistency.

**Citations — all preserved exactly, but three worth verifying:**

9. **[21] Raju & Vedaraj, *Frontiers in Mechanical Engineering* 12 (2026) 1886296.**
   Dated 2026 and therefore very recent. Confirm it is fully published (not accepted
   / in press) and that the volume and article number are final.
10. **[24] Sun et al., DOI `10.1109/tte.2022.3215691`** — the DOI carries 2022 while
    the citation gives 2023, which is normal for IEEE early access, but confirm the
    final volume/issue/pages. The DOI suffix is also lowercase (`tte`) where IEEE
    style is `TTE`; it resolves either way.
11. **One curly apostrophe** (U+2019, in the Table 2 footnote "each study's own
    baseline") against 16 straight apostrophes elsewhere. Normalise before submission.

**Methodological point a reviewer may raise:** §2.3 and §2.4 state that results were
extracted from **abstracts only**. You are commendably explicit about this, but for a
university review paper a marker may expect the headline numbers to come from the full
texts. Worth considering if you have time to verify the key figures.

**No fabricated content.** I added no facts, citations, authors, years, DOIs or
numerical values. Every claim in the revised text traces to the original.
