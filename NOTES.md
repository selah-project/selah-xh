# NOTES — selah-xh, chair 78

Working notes in English. The reader-facing documents (`README.md`,
`CONTRIBUTING.md`, `LICENSE.md`) are in isiXhosa, as this chair's own
documents should be. The full account of what went wrong and what was
decided is in `PROVENANCE.md`.

Lit 2026-09-18. Burn complete 2026-09-18; cleaned 2026-09-18 → 09-19.
Floor 23,213 verses.

Second **Nguni** chair, beside isiZulu — and the first chair since the
Latin run whose thermometer has **no closed-letter probe**: isiXhosa
shares its alphabet and its clicks with isiZulu, so the neighbour can
only be told apart by vocabulary.

---

## Burn signature

| | |
|---|---|
| relay | `batch/relay-move-on! [:xh]`, engine-side |
| after the relay | 23,124 / 23,213 — residue **89** |
| gleaning | `[32000 8000 48000 4000 24000]`, first success wins — all 89 landed |
| final | **23,213 / 23,213 verses** |

## The thermometer

Vocabulary, **whitelist first**. The isiZulu words the rails' table
names (`futhi`, `manje`, `lapho`, `ngoba`, `uma`, `yini`, `umuntu`,
`uNkulunkulu` … — the full list is in `dev/scripts/xh_gate.clj`) are
counted as whole words on **both surfaces**: the
reader's flow and the token row. The row thermometer found 72 isiZulu
glosses the flow count had missed. After the re-press: **zero**, with one
word held for a native ear (below).

## The Name

isiXhosa Bibles print **uYehova** and **iNkosi**. This chair writes
**uYahwe**, and keeps D1 for the rest: uElohim · u-Adonayi · uShadayi ·
uYah · u-El · u-Eloha · Tsebhayoti. `iNkosi` keeps its lawful seat over a human lord; the census
reads the token's Hebrew surface, never the spelling, and matches stems
case-sensitively (`Nkosi`, `Thixo`).

**Name seats reading uYahwe: 6,827 of 6,827.**

## Open seats — declared, not repaired

| seat | what | waiting on |
|---|---|---|
| malachi/3/1 · zechariah/4/14 | **אדון** used of Elohim — no D1 row; the chair wrote `iNkosi`, and the en floor's own row says *Lord* | a ruling on an אדון row |
| daniel/3/12 | `יתהון` — Aramaic's own object marker; glossed `bona` to match the en floor | the ruling on ית — 31 chairs mark it where the floor does not |
| daniel/5/23 | Aramaic **מרא** rendered `Nkosi` | the **D1 Aramaic row** — D1 covers Hebrew only |
| job/32/22 | `uMdali` (*my Maker*, עשני) — lawful: a participle, not a Name | — |
| 357 verses | the flow carries fewer ⟨את⟩ than its row (gap **390**) | a reader — see below |

### The ⟨את⟩ gap

isiXhosa fuses the object into the verb (`wababona` — *he-them-saw*), so
many rows carry a marker the flow has no separate word to hang it on.
**585** markers were placed programmatically, each only where the whole
verse could be proven aligned (a bare את marks the next word; a suffixed
form marks its own pronoun; whole word, exactly once, outside supplied
brackets, in row order). A re-press of 943 more brought the gap from
1,827 to **390**. That is inside the live fleet's range (zu 542 · am 231
· sv 212). None of the remaining 357 verses is placeable by proof; they
are left for a reader, not guessed.

## Held for a native ear

- **`yini`** — the rails list it as an isiZulu marker, but it may also be
  lawful isiXhosa as a question tag. Deut 32:6 was rewritten
  (`akanguye na`); the remaining occurrences stand until someone who
  speaks the language says.
- The coined method terms in the rails and the UI catalog —
  `ithokheni`, `umphezulu`, `inkcazelo`; `AMAGAMA ASINGATHAYO`
  (hostwords), `IZAKHI` (factors), `isiziba` (basin), `isalathiso`
  (concordance).
- The breastplate's gem names, against a printed Exodus 28.

## Hand seats

`xh_hand_pass.clj` — every edit presence-checked, both surfaces:

- 2-samuel/7/28 → `u-Adonayi` (the divine Adonai)
- numbers/32/25 → `iNkosi yam` (Moses, a man — the bracket removed)
- daniel/3/12 `יתהון` → `bona`
- genesis/30/31 `לך` → `kuwe` · 2-chronicles/21/12 and numbers/20/17
  `אשר` → `ukuba` (three hollow rows given the floor's word)
- psalms/56/14 — a stray `‹›` removed
- deuteronomy/32/6 — `yini` → `akanguye na`
- isaiah/26/20 — the **Hebrew surface** restored from the record
  (`חבiy` → `חבי`)
- 1-kings/10/5 — `seNkosi uYahwe`, the title fused onto the Name, found
  only by reading flows against rows (re-pressed, round three)
