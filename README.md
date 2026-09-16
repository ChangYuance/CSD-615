# CSD-615

**Chinese Stroke Dysarthria 615** — a Mandarin dysarthric speech corpus with independent severity ratings from three senior clinicians.

> Release page. Full audio is not hosted in this repository — see [Access](#access).
>
> Rendered version with inline audio players: **https://ChangYuance.github.io/CSD-615/**

---

## Overview

CSD-615 contains **615 Mandarin speech samples** collected from stroke patients across tertiary hospitals in China. Each participant performed a simple counting task — counting from one to ten in Mandarin through a dedicated mobile application.

Every sample was independently rated by **three chief physicians** with more than 10 years of stroke experience, on a four-level severity scale:

| Level | Label | Description |
|---|---|---|
| 0 | Normal | No dysarthria |
| 1 | Mild | Mild dysarthria |
| 2 | Moderate | Moderate dysarthria |
| 3 | Severe | Severe dysarthria |

We ship the **median** of the three ratings as the reference severity label.

What distinguishes CSD-615 from existing dysarthria corpora is that the **individual clinician ratings are released alongside the audio**, rather than only a single consensus label. This makes the corpus suitable for multi-annotator learning, label-noise research, and studies of inter-rater variability in perceptual dysarthria assessment.

---

## Sample audio

Two samples per severity level, all with **unanimous** ratings from the three clinicians (so the reference label is unambiguous). Audio is 16 kHz mono, converted from the original 48 kHz recordings.

### Normal (level 0)

| Sample | Sex | Duration | Listen |
|---|---|---|---|
| `normal_01` | F | 7.0 s | [▶ play](audio/normal_01.mp3) |
| `normal_02` | M | 7.0 s | [▶ play](audio/normal_02.mp3) |

### Mild (level 1)

| Sample | Sex | Duration | Listen |
|---|---|---|---|
| `mild_01` | F | 8.0 s | [▶ play](audio/mild_01.mp3) |
| `mild_02` | M | 8.0 s | [▶ play](audio/mild_02.mp3) |

### Moderate (level 2)

| Sample | Sex | Duration | Listen |
|---|---|---|---|
| `moderate_01` | F | 7.0 s | [▶ play](audio/moderate_01.mp3) |
| `moderate_02` | M | 7.0 s | [▶ play](audio/moderate_02.mp3) |

### Severe (level 3)

| Sample | Sex | Duration | Listen |
|---|---|---|---|
| `severe_01` | F | 8.0 s | [▶ play](audio/severe_01.mp3) |
| `severe_02` | M | 8.0 s | [▶ play](audio/severe_02.mp3) |

---

## Participant statistics

### Severity distribution and demographics

| Severity | Samples | Share | Sex (F / M) | Age (mean ± SD) | Unanimous ratings |
|---|---|---|---|---|---|
| Normal (0) | 458 | 74.5 % | 129 / 329 | 62.0 ± 11.5 | 421 (91.9 %) |
| Mild (1) | 43 | 7.0 % | 13 / 30 | 65.2 ± 10.7 | 12 (27.9 %) |
| Moderate (2) | 40 | 6.5 % | 17 / 23 | 65.4 ± 10.4 | 13 (32.5 %) |
| Severe (3) | 74 | 12.0 % | 30 / 44 | 64.5 ± 9.9 | 59 (79.7 %) |
| **All** | **615** | **100 %** | **189 / 426** | **62.8 ± 11.3** | **505 (82.1 %)** |

"Unanimous" means all three clinicians assigned the same level.

### Severity ratings by clinician

Each clinician's raw rating distribution over the 615 samples:

| Clinician | Level 0 | Level 1 | Level 2 | Level 3 |
|---|---|---|---|---|
| Clinician A | 439 | 32 | 41 | 103 |
| Clinician B | 471 | 53 | 29 | 62 |
| Clinician C | 462 | 38 | 41 | 74 |

Pairwise raw agreement: A–B **82.1 %**, A–C **87.2 %**, B–C **90.1 %**.

### Where the disagreement lives

Clinicians agree almost perfectly on clear cases and diverge sharply on borderline ones. Unanimous agreement is **91.9 %** for Normal and **79.7 %** for Severe, but collapses to **27.9 %** for Mild and **32.5 %** for Moderate — even though the three raters share the same training and protocol. The disagreements are overwhelmingly one level apart, concentrating on the Normal/Mild and Mild/Moderate boundaries.

This is the property that motivates releasing the individual ratings rather than a single consensus label.

---

## Recording conditions

| Property | Value |
|---|---|
| Language | Mandarin Chinese |
| Task | Counting 1–10 |
| Sample rate | 48 kHz (original), 16 kHz (samples above) |
| Channels | Mono |
| Bit depth | 16-bit PCM |
| Duration | 3–24 s (mean ≈ 7.7 s) |

Participants were recorded through a dedicated mobile application under a fixed protocol.

---

## Access

This repository hosts only the eight preview clips above.

The full 615-sample corpus, including the three individual clinician ratings per sample, is available for **non-commercial research use** upon request.

To request access, please open an issue in this repository or contact the authors with:

- your name and institutional affiliation,
- a short description of the intended research use,
- agreement to the terms of use below.

Requests are reviewed individually. Access may be granted subject to the terms of the original ethics approval.

---

## Ethics

All data were collected under institutional ethics approval with written informed consent from each participant. Participants consented to the use of their recordings for research purposes.

Audio previews in this repository are provided solely to illustrate the severity levels. They contain no personally identifying metadata: no participant identifiers, contact details, or hospital names are published. The preview clips are labelled with a within-repo index only.

---

## Terms of use

- Research use only. Commercial use is not permitted.
- Do not attempt to re-identify any participant.
- Do not redistribute the audio to third parties; direct them here instead.
- Any publication using this corpus must cite the paper below.

---

## Citation

```bibtex
@inproceedings{chang2027sedid,
  title     = {Learning from Clinician Severity Disagreement for Speech-Based Dysarthria Detection},
  author    = {Chang, Yuance and Ding, Han and Zhao, Cui and Wang, Fei and Wang, Ge and Wang, Zhi and Xi, Wei},
  booktitle = {Proceedings of IEEE ICASSP},
  year      = {2027}
}
```

### Samples by contributing site

The corpus was collected at ten tertiary hospitals. Sites are referred to by code
(`Hospital A`–`Hospital J`), ordered by number of samples; the names are withheld.

| Site | Samples | Share | Normal / Mild / Moderate / Severe | Sex (F / M) | Age (mean ± SD) |
|---|---|---|---|---|---|
| Hospital A | 186 | 30.2 % | 152 / 12 / 11 / 11 | 64 / 122 | 63.2 ± 11.5 |
| Hospital B | 111 | 18.0 % | 79 / 4 / 8 / 20 | 35 / 76 | 61.1 ± 11.9 |
| Hospital C | 89 | 14.5 % | 77 / 7 / 4 / 1 | 19 / 70 | 62.8 ± 10.6 |
| Hospital D | 69 | 11.2 % | 33 / 4 / 8 / 24 | 24 / 45 | 65.9 ± 11.1 |
| Hospital E | 55 | 8.9 % | 38 / 5 / 5 / 7 | 16 / 39 | 61.9 ± 12.0 |
| Hospital F | 52 | 8.5 % | 41 / 8 / 2 / 1 | 16 / 36 | 62.7 ± 10.2 |
| Hospital G | 16 | 2.6 % | 12 / 1 / 1 / 2 | 3 / 13 | 58.4 ± 9.1 |
| Hospital H | 16 | 2.6 % | 10 / 1 / 1 / 4 | 6 / 10 | 65.6 ± 11.0 |
| Hospital I | 12 | 2.0 % | 8 / 0 / 0 / 4 | 4 / 8 | 63.8 ± 10.8 |
| Hospital J | 9 | 1.5 % | 8 / 1 / 0 / 0 | 2 / 7 | 57.0 ± 4.9 |
| **All** | **615** | **100 %** | **458 / 43 / 40 / 74** | **189 / 426** | **62.8 ± 11.3** |

Severity mix varies substantially across sites — from 1 % severe at Hospital C to 35 %
at Hospital D — so site is a meaningful source of heterogeneity in this corpus. Note that
several sites contribute few samples (Hospital I: 12, Hospital J: 9), so per-site severity
proportions for those sites are unstable and should not be over-interpreted.
