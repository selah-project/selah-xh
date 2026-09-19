# PROVENANCE — how this rendering came to be

*isiXhosa, chair 78. Lit 2026-09-18. Floor 23,213 verses.*

This is the record of how the text in this repository was produced and
what went wrong with it. A machine-assisted rendering has no standing
unless you can see how it was made, so this file says both.

---

## The approach

Every verse is rendered from the Hebrew of that verse, under a written
discipline — `docs/methodology/translation-discipline/xh.md` in the Selah
repository, itself written in isiXhosa and mirroring the sister chair
`zu.md`. Six rules govern it: the Hebrew token is the unit; the Name stays
the Name; both truths of Deut 6:4; no foreknowledge (Gen 22:1 does not
know Gen 22:13); numbers and marks stay put; the translator has no word
of its own.

**The `⟨ ⟩` brackets do two different jobs.** `⟨את⟩` is the Hebrew
direct-object marker, which isiXhosa has no word for; it is left standing
so the reader sees it. `⟨igama⟩` is a word Hebrew did not write but
isiXhosa grammar requires — visibly marked, so you can always tell what
the Hebrew said from what the grammar needed.

## The fight on this chair is the Name

| Hebrew | here | rejected |
|---|---|---|
| יהוה | **uYahwe** | uYehova, iNkosi, uThixo |
| אלהים | **uElohim** | uThixo in the Name's place |
| אדני | **u-Adonayi** | iNkosi |
| שדי | **uShadayi** | "uSomandla" as a substitute |
| אל | **u-El** | "uthixo" as a type-name |

`iNkosi` over a human lord and lowercase `oothixo` for the nations' gods
remain lawful; the census applies that distinction by the token's Hebrew
surface, never by spelling.

## The burn and the gate

The relay rendered 23,124 of 23,213 verses and moved on with a residue of
**89**; the gleaning ladder `[32000 8000 48000 4000 24000]` landed all of
them. A first-hour gate (`dev/scripts/xh_gate.clj`) — the Name, the את
family, isiZulu words, thirteen marquee verses — passed at 11,860 verses
and was re-run every half hour to the end.

The corpus was committed to git **before any pass touched it**
(`f2a43b7f`), so every repair below is a diff you can read.

## Finding: letters that only look Latin

103 verses carried Cyrillic, Greek or mathematical-italic letters inside
otherwise Latin words (`uthе` with a Cyrillic *е*). They defeat every
search that would find them, so they were cured first
(`xh_homoglyph_repair.clj`): a foreign letter is mapped to its Latin twin
only inside a word that already carries Latin.

## Finding: the thermometer has two surfaces

The isiZulu count was first taken on the reader's flow. Taken again on
the token row, it found **72** isiZulu glosses the flow count had missed —
the row had the neighbour's word while the flow, written afterwards, had
the right one. Every census class on this chair is read on both surfaces.

## Finding: a marker tool that guessed

The fleet's tool for restoring a lost ⟨את⟩ to the flow placed it at the
first substring match, falling back to the first word. A spot-check of
three verses found three wrong — a doubled marker, a marker on the
subject, a marker mid-phrase — because an agglutinative language hides
the object inside the verb. The pass was reverted whole. Its replacement
(`selah.translate.flow-markers`) writes a marker only when the entire
verse can be proven aligned, and otherwise writes nothing. 585 placed;
the rest re-pressed or left for a reader (see NOTES.md).

## The cure, in order

| pass | what |
|---|---|
| gleaning ladder | 89 residue seats |
| homoglyphs | 103 verses |
| re-press 1 | **790** census-convicted seats (press 730 · ladder 60) |
| re-press 2 | **133** — the isiZulu the row thermometer found, the last script leaks, the Name's stragglers |
| hand pass | 2 Sam 7:28 · Num 32:25 · Dan 3:12 |
| re-press 3 | **23** — the last hollow glosses, and three seats found by reading flows against rows |
| hand pass 4 | three hollow rows · Ps 56:14 · Deut 32:6 · Isa 26:20's Hebrew surface |
| flow markers | **585** placed by proof |
| re-press 5 | **943** verses whose flows had lost ⟨את⟩ (press 898 · ladder 45) |

## Open — declared, not repaired

- **אדון of Elohim** — Mal 3:1, Zech 4:14. No D1 row.
- **Aramaic** — Dan 3:12 `יתהון`, Dan 5:23 `מרא`. D1 covers Hebrew only.
- **The ⟨את⟩ gap** — 390 markers across 357 verses, unplaceable by proof.
- **`yini`**, the coined terms, the gem names — a native ear.

## Final

**23,213 / 23,213 verses.** uYahwe in **6,827 of 6,827** Name seats.
Every census class zero except the declared marker gap. isiZulu on
either surface: **0**, `yini` held.
