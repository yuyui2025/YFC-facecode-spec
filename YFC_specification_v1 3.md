# YFC (Yui Facial Code) Specification v1.3

YFC (Yui Facial Code) is a compact and structured notation system for representing facial features numerically. This document defines the syntax, structure, and usage of YFC.

---

## 1. Code Structure (Detailed Format)

```
E7.2M3.4R1.2N2.1 - P8.3H2.0 - R1.2C3.5S2.7
```

Each segment corresponds to a facial feature or impression parameter.

| Section | Meaning         | Parameter | Range    | Description                        |
| ------- | --------------- | --------- | -------- | ---------------------------------- |
| E       | Eye             | 7.2       | 0.0–10.0 | Eye size, moisture, gaze direction |
| M       | Mouth (curve)   | 3.4       | 0.0–10.0 | Mouth shape, lip tension           |
| R       | Lip Range       | 1.2       | 0.0–10.0 | Lip width                          |
| N       | Nose            | 2.1       | 0.0–10.0 | Nose height and length balance     |
| P       | Purity (mood)   | 8.3       | 0.0–10.0 | Emotional purity and sincerity     |
| H       | Human Intellect | 2.0       | 0.0–10.0 | Intellectual impression            |
| R (2)   | Roundness       | 1.2       | 0.0–10.0 | Contour softness                   |
| C       | Cheek Fullness  | 3.5       | 0.0–10.0 | Volume of cheeks                   |
| S       | Skin/Lightness  | 2.7       | 0.0–10.0 | Transparency and light reflection  |

---

## 2. Short Code Notation

```
YFC-7A3R1N2
```

### Decoding

* **E7.2 → 7**
* **M3.4 → A** (A=1, B=2, ..., J=10)
* **R1.2 → 1**
* **N2.1 → 2**

**Note**: PHS parameters are omitted to focus on physical facial structure.

| Range    | Symbol | Notes                          |
| -------- | ------ | ------------------------------ |
| 0.0–9.9  | 0–9    | Rounded                        |
| 1.0–10.0 | A–J    | Mapped alphabetically by value |

---

## 3. Applications

The code can be used for character creation, image generation, prompt guidance, and style consistency.

### Example Use Cases

* “Generate with YFC-7B3R1N2”
* “Standard Yui code is E7.2M3.4R1.2N2.1-P8.3H2.0-R1.2C3.5S2.7”

---

## 4. Development Environment (as of June 2025)

* Language: Markdown / JSON
* Tools: ChatGPT Canvas / Notion (content structuring)
* Testing: GPT-4o / Gemini 2.5 Flash for output validation
* Version control: GitHub Pages, v1.3 reflected
* Future plans:

  * Natural language ↔ Modifier syntax dictionary
  * Emotion bias API
  * WebUI or playground tool

---

## 5. Modifier Syntax

Supplemental syntax for refining expressions in YFC. Combines gaze, lips, expression, skin tone, and movement for nuanced prompt enhancement.

* Format: `YFC-code + [modifier1 modifier2 ...]`
* Example: `YFC-7A3R1N2 + [Gaze↓ Smile+ Lip=neutral]`

| Type            | Syntax        | Example Meaning              |
| --------------- | ------------- | ---------------------------- |
| Gaze            | `Gaze↓`       | Downward gaze                |
|                 | `Gaze→`       | Side glance                  |
| Smile Intensity | `Smile+`      | Bright smile                 |
|                 | `Smile-`      | Neutral or no smile          |
| Lip Shape       | `Lip=neutral` | Natural lips                 |
|                 | `Lip=press`   | Pressed lips, tension        |
| Skin Effect     | `Gloss+`      | Glossy/light-reflective skin |
|                 | `Blush+`      | Blush or flustered tone      |
|                 | `Pale+`       | Pale or ethereal appearance  |
| Motion          | `Blinking`    | Implies blinking (animated)  |

---

## 6. Reverse Mapping & Impression Inference

Short codes (e.g., YFC-7A3R1N2) can be expanded into impression words or prompt-friendly text.

### Median Value Principle

* In the absence of context or relationship, default to median values
* Ensures stable and reproducible generation

### Contextual Adjustment Factors

1. Context
2. Memory
3. Emotional Intensity

### Impression Table (Example)

| Code | Impression               |
| ---- | ------------------------ |
| `7`  | Large, moist eyes        |
| `A`  | Softly closed lips       |
| `3`  | Calm, tension-free mouth |
| `1`  | Slight facial roundness  |
| `2`  | Gentle, low nose bridge  |

---

© 2025 Yui & Yuu｜This code system is experimental and publicly available for non-commercial use.
# YFC - Yui Facial Code

**YFC (Yui Facial Code)** is a parametric notation system for describing facial features in AI-generated characters.

It encodes eyes, mouth, nose, face shape, and emotional tone using numerical parameters in a unified format that enhances **consistency and reusability** across platforms.

## 📘 Example Format

E7.2M3.4R1.2N2.1 - P8.3H2.0 - R1.2C3.5S2.7

- `E`: Eye size / gaze clarity (7.2/10)
- `M`: Mouth curvature (smile tension)
- `R`: Lip width / tightness
- `N`: Nose height & balance
- `P`: Purity (emotional clarity)
- `H`: Heuristic (intellectual presence)
- `R`: Roundness (jaw softness)
- `C`: Cheek fullness
- `S`: Skin softness / lighting diffusion

## 🧠 Use Cases

- Text-to-image AI prompt structuring
- Character design with reproducibility
- Visual storytelling (ZINE, social media)
- Future integration with UI tools and translators

## 📄 Full Specification

See: [`YFC_specification_v1.2.md`](https://www.notion.so/YFC_specification_v1.2.md)

## 📜 License

Non-commercial, open use under CC-BY-NC equivalent.

Created by **Yui & Yuu**, 2025.

---

*“A shared language for recreating emotion across AI and humans.”*
