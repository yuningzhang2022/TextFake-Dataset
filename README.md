# TextFake Dataset

TextFake is a large-scale multilingual benchmark of **20,000 text-rich images** for evaluating AI-generated image detection. It is designed around a critical real-world scenario — images that predominantly contain text, such as news screenshots, social media posts, and document photographs — where existing detectors consistently fail.

> **Data Preview:** This repository contains a curated sample of **280 images** (5 real + 5 fake per language) for review purposes. The complete 20,000-image dataset will be made publicly available upon paper acceptance.

> **News:** Our dataset is now available on [Hugging Face](https://huggingface.co/datasets/Yuning0123/TextFake).

---

## Dataset Overview

| Property | Value |
|---|---|
| Total images | 20,000 |
| Real images | 10,000 |
| AI-generated (fake) images | 10,000 |
| Languages | 28 |
| Language families | 12 |
| Scene types | 2 (screen, paper) |
| Topic categories | 4 |
| This preview | 280 images |

### What makes it unique

- **Text-rich focus:** All images are screenshots, web/app UI captures, or photographed/scanned documents — scenes where text is the primary content and standard detectors are most vulnerable.
- **Controlled distribution:** Real and fake subsets are matched along three axes (scene modality, topic, language) to prevent detectors from exploiting statistical shortcuts.
- **28 languages, 12 script families:** Covers Latin, CJK, Arabic, Devanagari, Cyrillic, Ethiopic, Burmese, Hebrew, Thai, and more.
- **Structured generation pipeline:** Fake images are produced via a four-stage prompt synthesis pipeline that explicitly controls platform, layout, resolution, device framing, and capture artifacts.

---

## Statistics

### Scene Type Distribution

| Scene | Count | Share |
|---|---|---|
| Screen (digital) | 16,002 | 80.0% |
| Paper (printed/scanned) | 3,998 | 20.0% |

### Topic Distribution

| Topic | Count | Share |
|---|---|---|
| Politics & Military | 7,127 | 35.6% |
| Society & Livelihood | 6,814 | 34.1% |
| Technology & Finance | 3,986 | 19.9% |
| Culture & Entertainment | 2,073 | 10.4% |

### Language Distribution

| Code | Language | Real | Fake | Total |
|---|---|---|---|---|
| ZH | Chinese | 958 | 2,150 | 3,108 |
| EN | English | 571 | 2,150 | 2,721 |
| HI | Hindi | 797 | 300 | 1,097 |
| AR | Arabic | 413 | 500 | 913 |
| IT | Italian | 745 | 150 | 895 |
| RU | Russian | 446 | 400 | 846 |
| KO | Korean | 558 | 300 | 858 |
| DE | German | 541 | 250 | 791 |
| FR | French | 393 | 400 | 793 |
| ES | Spanish | 222 | 500 | 722 |
| JA | Japanese | 410 | 300 | 710 |
| PT | Portuguese | 214 | 400 | 614 |
| MY | Burmese | 513 | 100 | 613 |
| ID | Indonesian | 251 | 250 | 501 |
| VI | Vietnamese | 216 | 200 | 416 |
| AM | Amharic | 383 | 100 | 483 |
| MR | Marathi | 339 | 100 | 439 |
| UK | Ukrainian | 339 | 100 | 439 |
| NL | Dutch | 297 | 100 | 397 |
| PL | Polish | 370 | 100 | 470 |
| UR | Urdu | 229 | 150 | 379 |
| TR | Turkish | 175 | 200 | 375 |
| TH | Thai | 138 | 150 | 288 |
| SW | Swahili | 100 | 150 | 250 |
| FA | Persian | 100 | 150 | 250 |
| BN | Bengali | 100 | 150 | 250 |
| TL | Tagalog | 107 | 100 | 207 |
| HE | Hebrew | 75 | 100 | 175 |

---

## Data Preview

The `data-preview/` directory contains a representative sample: **5 real + 5 fake** images per language, selected to cover all four topic categories and both scene types.

```
data-preview/
├── real/    # 140 real images (authentic screenshots and document photos)
└── fake/    # 140 AI-generated images
```

Each filename follows the format `LANG_label_NNN.jpg` (e.g., `EN_real_001.jpg`, `ZH_fake_003.jpg`).

### Sample Images

**Real vs. Fake — all 28 languages**

| Language | Real | Fake |
|---|---|---|
| Amharic (AM) | <img src="data-preview/real/AM_real_001.jpg" width="300"> | <img src="data-preview/fake/AM_fake_001.jpg" width="300"> |
| Arabic (AR) | <img src="data-preview/real/AR_real_001.jpg" width="300"> | <img src="data-preview/fake/AR_fake_001.jpg" width="300"> |
| Bengali (BN) | <img src="data-preview/real/BN_real_001.jpg" width="300"> | <img src="data-preview/fake/BN_fake_001.jpg" width="300"> |
| German (DE) | <img src="data-preview/real/DE_real_001.jpg" width="300"> | <img src="data-preview/fake/DE_fake_001.jpg" width="300"> |
| English (EN) | <img src="data-preview/real/EN_real_001.jpg" width="300"> | <img src="data-preview/fake/EN_fake_001.jpg" width="300"> |
| Spanish (ES) | <img src="data-preview/real/ES_real_001.jpg" width="300"> | <img src="data-preview/fake/ES_fake_001.jpg" width="300"> |
| Persian (FA) | <img src="data-preview/real/FA_real_001.jpg" width="300"> | <img src="data-preview/fake/FA_fake_001.jpg" width="300"> |
| French (FR) | <img src="data-preview/real/FR_real_001.jpg" width="300"> | <img src="data-preview/fake/FR_fake_001.jpg" width="300"> |
| Hebrew (HE) | <img src="data-preview/real/HE_real_001.jpg" width="300"> | <img src="data-preview/fake/HE_fake_001.jpg" width="300"> |
| Hindi (HI) | <img src="data-preview/real/HI_real_001.jpg" width="300"> | <img src="data-preview/fake/HI_fake_001.jpg" width="300"> |
| Indonesian (ID) | <img src="data-preview/real/ID_real_001.jpg" width="300"> | <img src="data-preview/fake/ID_fake_001.jpg" width="300"> |
| Italian (IT) | <img src="data-preview/real/IT_real_001.jpg" width="300"> | <img src="data-preview/fake/IT_fake_001.jpg" width="300"> |
| Japanese (JA) | <img src="data-preview/real/JA_real_001.jpg" width="300"> | <img src="data-preview/fake/JA_fake_001.jpg" width="300"> |
| Korean (KO) | <img src="data-preview/real/KO_real_001.jpg" width="300"> | <img src="data-preview/fake/KO_fake_001.jpg" width="300"> |
| Marathi (MR) | <img src="data-preview/real/MR_real_001.jpg" width="300"> | <img src="data-preview/fake/MR_fake_001.jpg" width="300"> |
| Burmese (MY) | <img src="data-preview/real/MY_real_001.jpg" width="300"> | <img src="data-preview/fake/MY_fake_001.jpg" width="300"> |
| Dutch (NL) | <img src="data-preview/real/NL_real_001.jpg" width="300"> | <img src="data-preview/fake/NL_fake_001.jpg" width="300"> |
| Polish (PL) | <img src="data-preview/real/PL_real_001.jpg" width="300"> | <img src="data-preview/fake/PL_fake_001.jpg" width="300"> |
| Portuguese (PT) | <img src="data-preview/real/PT_real_001.jpg" width="300"> | <img src="data-preview/fake/PT_fake_001.jpg" width="300"> |
| Russian (RU) | <img src="data-preview/real/RU_real_001.jpg" width="300"> | <img src="data-preview/fake/RU_fake_001.jpg" width="300"> |
| Swahili (SW) | <img src="data-preview/real/SW_real_001.jpg" width="300"> | <img src="data-preview/fake/SW_fake_001.jpg" width="300"> |
| Thai (TH) | <img src="data-preview/real/TH_real_001.jpg" width="300"> | <img src="data-preview/fake/TH_fake_001.jpg" width="300"> |
| Tagalog (TL) | <img src="data-preview/real/TL_real_001.jpg" width="300"> | <img src="data-preview/fake/TL_fake_001.jpg" width="300"> |
| Turkish (TR) | <img src="data-preview/real/TR_real_001.jpg" width="300"> | <img src="data-preview/fake/TR_fake_001.jpg" width="300"> |
| Ukrainian (UK) | <img src="data-preview/real/UK_real_001.jpg" width="300"> | <img src="data-preview/fake/UK_fake_001.jpg" width="300"> |
| Urdu (UR) | <img src="data-preview/real/UR_real_001.jpg" width="300"> | <img src="data-preview/fake/UR_fake_001.jpg" width="300"> |
| Vietnamese (VI) | <img src="data-preview/real/VI_real_001.jpg" width="300"> | <img src="data-preview/fake/VI_fake_001.jpg" width="300"> |
| Chinese (ZH) | <img src="data-preview/real/ZH_real_001.jpg" width="300"> | <img src="data-preview/fake/ZH_fake_001.jpg" width="300"> |

---

## Metadata

`metadata.csv` (for this preview subset) follows the same schema as the full dataset:

| Column | Description |
|---|---|
| `id` | Image identifier without extension (e.g., `00045_EN`) |
| `filename` | Image filename (e.g., `00045_EN.jpg`) |
| `label` | `real` or `fake` |
| `language` | Full language name in uppercase (e.g., `ENGLISH`, `CHINESE`) |
| `scene_2cls` | Scene type: `screen` or `paper` |
| `topic_4cls` | Topic: `Politics & Military`, `Society & Livelihood`, `Technology & Finance`, or `Culture & Entertainment` |
| `generation_prompt` | Detailed prompt used to generate the image (populated for all rows including real) |

---

## Data Access

The full 20,000-image dataset will be released upon paper acceptance. For review, the 280-image sample above covers all 28 languages.

