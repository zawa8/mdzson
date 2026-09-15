# HSKII Encoding Documentation
## Overview of Hindi Phonetics & Hexadecimal Encoding Design

This document details the architecture of the **HSKII encoding system**. The system achieves structural balance by cleanly dividing uppercase and lowercase characters between base phonetic sounds, aspirated/modified sounds, and hexadecimal numeric digits (10–15). 

---

## 1. Character Categorization Matrix

The 44-character framework is structurally divided into three core sets, preventing overlap between phonetic representations and hex digits.

### Base Phonetic Sounds (26 Lowercase/Vowels)
* `a`, `i`, `u`, `e`, `o` (Vowels)
* `k`, `g`, `c`, `z`, `t`, `d`, `T`, `D`, `p`, `b`, `s`, `n`, `r`, `v`, `y`, `w`, `l` (Consonants)

### Aspirated & Modified Phonetic Sounds (12 Capitals + `f`)
* **Capitalized Consonants:** Reused strictly for aspirated or altered native Hindi phonemes (e.g., `k` $\rightarrow$ क, `K` $\rightarrow$ ख).
* **Special Case `f`:** Mapped as the aspirated variant of `p` ($f = ph = $ फ).

### Reused Hexadecimal Digits (6 Capitals)
* **Reused Set:** `L`, `Y`, `V`, `W`, `P`, `F`
* **Design Logic:** In human speech, these capital letters do not represent a phonetically distinct sound from their lowercase counterparts (`l`, `y`, `v`, `w`, `p`, `f`). They are completely **free** to be mapped as base-16 single-character digits (10–15) without causing semantic parsing ambiguity in phonetic strings.

---

## 2. Hexadecimal Digit Assignment & Mnemonics

The hex characters `L Y V W P F` correspond to the base-10 values 10 through 15. Their design leverages arithmetic alignment and intuitive phonetic mnemonics.

### Mathematical Shifts
* `L` + 6 = `F` $(10 + 6 = 16 \equiv 0 \pmod{16})$
* `Y` + 5 = `F` $(11 + 5 = 16)$
* `V` + 4 = `F` $(12 + 4 = 16)$
* `W` + 3 = `F` $(13 + 3 = 16)$
* `P` + 2 = `F` $(14 + 2 = 16)$
* `F` + 1 = `F + 1` = $16 \rightarrow$ `10` (Generates a carry)

### Mnemonic Derivations
* **L** = Ten $\rightarrow$ Derived from $8 + 2 = F - 1$
* **Y** = Yilewen $\rightarrow$ Sounds like "eleven" ($L + 1$)
* **V** = Twelw $\rightarrow$ Represents 12 (Roman numeral V = 5, modified here to $L + 2$, structural link: $v \rightarrow$ ह, $V = 8 + 4 = 12$)
* **W** = Dblun $\rightarrow$ Double-u / Fourteen variant structural step ($L + 3$)
* **P** = Purxn $\rightarrow$ Fourteen ($L + 4$)
* **F** = Fiwxn $\rightarrow$ Fifteen ($L + 5$)

---

## 3. Detailed Mapping Tables

### Allowed Hexadecimal Mappings (Free Phonetic Status)

| Hex Value | Letter | Phonetic Status / Justification |
| :--- | :--- | :--- |
| **10** | **L** | Same acoustic footprint as lowercase `l` — Free to use |
| **11** | **Y** | Same acoustic footprint as lowercase `y` — Free to use |
| **12** | **V** | Same acoustic footprint as lowercase `v` — Free to use |
| **13** | **W** | Same acoustic footprint as lowercase `w` — Free to use |
| **14** | **P** | Same acoustic footprint as lowercase `p` — Free to use |
| **15** | **F** | Same acoustic footprint as lowercase `f` — Free to use |

### Reserved Phonetic Mappings (Explicitly Excluded from Hex)

These keys are completely frozen and cannot be utilized as hex values due to strict structural requirements for aspirated pairs and specialized nasal sounds.

| Letter | Devanagari Character | Phonetic Properties & Description |
| :--- | :--- | :--- |
| `k` | **क** | Unaspirated velar plosive (e.g., कबूतर) |
| `K` | **ख** | Aspirated velar plosive (e.g., खरगोश) |
| `g` | **ग** | Voiced unaspirated velar plosive |
| `G` | **घ** | Voiced aspirated velar plosive |
| `c` | **च** | Unaspirated palatal affricate |
| `C` | **छ** | Aspirated palatal affricate |
| `z` | **ज** | Voiced unaspirated palatal affricate |
| `Z` | **झ** | Voiced aspirated palatal affricate |
| `t` | **ट** | Unaspirated retroflex plosive |
| `T` | **त** | Unaspirated dental plosive |
| `d` | **ड** | Voiced unaspirated retroflex plosive |
| `D` | **द** | Voiced unaspirated dental plosive |
| `j` | **थ** | Aspirated dental plosive |
| `J` | **ठ** | Aspirated retroflex plosive |
| `q` | **ध** | Voiced aspirated dental plosive |
| `Q` | **ढ** | Voiced aspirated retroflex plosive |
| `b` | **ब** | Voiced unaspirated bilabial plosive |
| `B` | **भ** | Voiced aspirated bilabial plosive |
| `s` | **स** / **ष** | Alveolar / Retroflex voiceless fricative |
| `S` | **श** | Palatal voiceless fricative |
| `r` | **र** | Alveolar trill / tap |
| `R` | **ड़** / **ढ़** | Retroflex flap / Aspirated retroflex flap |
| `n` | **न** | Alveolar nasal |
| `N` | **ं** | Anusvara (Special context-sensitive nasalization like `[ŋ]` before velars) |

---

## 4. Architectural Summary

$$\text{Total Characters (44)} = \underbrace{26}_{\text{Base (aiueoN kgcztdTDpbs)}} + \underbrace{12}_{\text{Capitals + f (Aspirated)}} + \underbrace{6}_{\text{Capitals (Hex Digits Dual-Use)}}$$

The design successfully prevents conflict between text strings and numeric metrics, maintaining full compatibility within the **38-sound HSKII font system boundary**.
