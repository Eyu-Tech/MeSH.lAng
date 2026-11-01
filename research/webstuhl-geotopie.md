# Webstuhl and Geotopie: measurements and examples

These examples connect the language concepts to existing software and recorded experiments. They cover different implementation stages and retain the original measurement conditions.

## W2 — Historical Webstuhl calibration

The calibration completed on **11 September 2026**, using Weberei revision `776ff3c` and an executable identified in the original receipt by SHA-256 `D89ED9D297989DC6239E9F0E458AFAC5900D26742A03E9DBD991FA8BF4B9405B`.

Its configured geometry was **512 bits**, basis seed **12648430**, n-gram length **3**, with two text projections:

- `identity-unicode-scalar-v1`: preserve the input scalar sequence;
- `unicode-nfc-lower-v1`: apply the declared normalization and lowercase projection.

| Recorded item | Result |
|---|---:|
| Prepared calibration cases | 30 passed, 0 failed |
| Meaning-bearing runs represented | 64 |
| Address scopes | 128 |
| Reading observations | 8,191 |
| Raw-to-anchored trajectory pairs | 1,151 |
| Field pre-to-post trajectory pairs | 2,048 |
| Total trajectory pairs | 3,199 |

One address had 63 readings and the other 127 had 64. The missing observation was retained as missing. The full within-scope comparison case emitted **524,161 comparisons per projection**, with **zero cross-scope comparison records**.

The trajectory consistency case checked all **3,199 pairs per projection** and recorded **zero mismatches**. This is a processing-consistency check, not a semantic agreement rate between agents.

## What a distance means in practice

The following values are Hamming distances in the configured 512-bit projection. They are measurements of the projected expressions, not calibrated percentages of semantic equivalence.

| Inputs | Identity projection | NFC/lowercase projection | What the example makes visible |
|---|---:|---:|---|
| `Kraft` / `kraft` | 111 bits | 0 bits | Case affects the identity representation |
| `ä` / `a` + combining diaeresis | 257 bits | 0 bits | Canonically equivalent spellings become equal under NFC |
| `Straße` / `Strasse` | — | 205 bits | Lowercasing is not a transliteration rule |
| `Ä` / `AE` | — | 251 bits | Umlaut transliteration is not performed |
| `Schmiede-Kraft` / `SchmiedeKraft` | 122 bits | — | A separator changes the represented sequence |
| `Kraft/Fluss` / `Kraft(Fluss)` | 165 bits | — | Different composition punctuation remains visible |

A dash marks a value not selected for this excerpt. The [CSV excerpt](webstuhl-calibration-excerpt.csv) preserves the individual selected case IDs and values.

The practical lesson is that the projection is part of the measurement contract. A zero after normalization has a defined cause; it does not prove identical real-world meaning.

## DSP in this development context

The surrounding architecture uses **DSP** for **Deterministic Semantic Processor**. It is the project's term, rather than a claim that these records are a conventional digital-signal-processing benchmark.

The implemented comparison apparatus provides deterministic symbolic projections, exact bit-distance records, scope-bound comparison matrices and paired trajectory analysis. In the wider vector implementation, composition and sequence/container operations provide additional processing building blocks.

These mechanisms make representations and their changes inspectable. Semantic interpretation is evaluated against explicit relationships, teaching conditions and task outcomes, as described in the [language research overview](overview.md).

## W3 — Native tensor examples

The Geotopie visualization source records three executed reference demonstrations:

1. **Tensor composition:** the 16-byte input `Rauscherzeugende` is displayed through native tensor composition.
2. **Persistence:** a native reference run displays the accepted source and changes in its image bank, frame, graph and file-arrival structures.
3. **Continuation:** a fixed native test accepts hexadecimal bytes `10 11` and then `12 13`, replacing the open frontier and extending the composed images.

The Geotopie dictionary adapter also accepts original file bytes, prepares its searchable representation once and returns source positions, byte offsets and native distances on subsequent searches. A zero maximum distance selects exact native agreement. Unicode content is retained as its original bytes in this path.

These native examples demonstrate implemented tensor, storage and lookup operations. The migration sources keep full continuous recursive inline checking separate from the completed dictionary integration.

## Reading the backend comparison

The shared architectural responsibilities are source intake, ordered composition, context preservation and comparison. An adapter realizes those responsibilities using the backend's own operations. The earlier VSA/HDC implementation and the Geotopie integration provide evidence at different coverage levels.

There is no matched VSA-versus-Geotopie speedup measurement in this excerpt. Recorded 512-bit distances are not relabeled as native tensor distances, and no numerical threshold is transferred between them.

## Provenance

**W2** denotes the original Webstuhl calibration receipt and case results. **W3** denotes the Geotopie migration/visualization documentation and executed reference views. These source IDs are resolved in the private publication provenance map. Full raw archives, private language mappings and implementation internals are not bundled here.

The values above are transcribed from existing records; no new benchmark run was performed for this publication draft.
