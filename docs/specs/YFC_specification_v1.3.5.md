# YFC (Yui Facial Code) Specification v1.3.5

**YFC (Yui Facial Code)** is a syntax for structurally describing and reproducing facial features and impressions using alphanumeric codes. This document defines the syntax, transformation rules, modifier extensions, and use cases suitable for implementation in machine learning and AI-related visual generation environments.

---

## 1. Code Format

```yfc
E7.2M3.4R1.2N2.1-P8.3H2.0-R1.2C3.5S2.7
```

### Code Sections

| Code | Name            | Example | Range    | Description                       |
| ---- | --------------- | ------- | -------- | --------------------------------- |
| E    | Eye             | 7.2     | 0.0–10.0 | Size, moisture, gaze direction    |
| M    | Mouth Curve     | 3.4     | 0.0–10.0 | Lip curvature, softness           |
| R    | Lip Width       | 1.2     | 0.0–10.0 | Width of lips                     |
| N    | Nose            | 2.1     | 0.0–10.0 | Height and length balance         |
| P    | Purity (Mood)   | 8.3     | 0.0–10.0 | Emotional transparency, innocence |
| H    | Human Intellect | 2.0     | 0.0–10.0 | Impression of rationality         |
| R(2) | Roundness       | 1.2     | 0.0–10.0 | Contour softness                  |
| C    | Cheek Fullness  | 3.5     | 0.0–10.0 | Volume of cheeks                  |
| S    | Skin/Lightness  | 2.7     | 0.0–10.0 | Transparency and reflectiveness   |

All values are interpreted as fractions of 10 (i.e., `x/10`).

---

## 2. Shorthand Format

```yfc
YFC-7A3R1N2
```

### Encoding Rules

* `E7.2 → 7`
* `M3.4 → A` (A = 1, B = 2, ..., J = 10)
* `R1.2 → 1`
* `N2.1 → 2`

| Value Range | Symbol | Note                                     |
| ----------- | ------ | ---------------------------------------- |
| 0.0–9.9     | 0–9    | Rounded to nearest integer               |
| 1.0–10.0    | A–J    | Rounded first decimal mapped to alphabet |

---

## 3. Modifiers

Modifiers refine the YFC code by appending expressive and surface traits. Use square brackets to encapsulate modifiers.

```yfc
YFC-7A3R1N2 + [Gaze↓ Smile+ Lip=press]
```

### Modifier Categories

* **Emotion**: `Smile`, `Tear`, `Anger`, `Sad`, `Fear`, `Joy`, `Surprise`
* **Gaze**: `Gaze↑`, `Gaze↓`, `Gaze→`, `Gaze←`, `GazeAway`, `GazeClose`
* **Lip/Mouth**: `Lip=curve`, `Lip=press`, `Mouth=open`, `Mouth=closed`
* **Texture/State**: `Blush`, `Blush+`, `Pale`, `Gloss`, `Sweat`, `TearTrail`

### Intensity Levels

| Symbol | Strength | Example Expression      |
| ------ | -------- | ----------------------- |
| `+`    | Low      | Gentle smile, soft glow |
| `++`   | Medium   | Defined emotion         |
| `+++`  | Strong   | Crying, visible tension |

---

## 4. Syntax Compression

* Mutually exclusive modifiers are pruned: `Gaze↑` vs. `Gaze↓`
* Redundant synonyms are merged: `Smile+` ≈ `Lip=curve+`

### Example

```yfc
[Smile+, Gaze→, Blush+] → YFC-A2
```

---

## 5. Applications

* Prompting AI with `YFC-7B3R1N2`
* Defining canonical characters: `E7.2M3.4R1.2N2.1-P8.3H2.0-R1.2C3.5S2.7`

### Use Case Domains

* Facial generation in AI platforms
* Avatar and character design
* Social media tagging
* Interactive fiction or ZINE production

---

## 6. Reverse Mapping

### Default Principle

When contextual data is missing, use median values for decoding.

### Bias Adjustment Factors

1. **Context** — scene, usage, surrounding modifiers
2. **Memory** — prior character patterns
3. **Emotion Intensity** — signal emphasis level

### Estimated Impressions

| Symbol | Approx. Value | Description          |
| ------ | ------------- | -------------------- |
| `7`    | E7.0–7.4      | Large, watery eyes   |
| `A`    | M3.0–3.9      | Soft, closed mouth   |
| `3`    | R2.5–3.4      | Relaxed lips         |
| `1`    | R1.0–1.4      | Rounded face outline |
| `2`    | N2.0–2.4      | Gentle nose line     |

---

## 7. Generation Models

* **Goal-Based**: From intent to structure
* **Reverse Mapping**: From image to code
* **Hybrid**: Round-trip optimization between form and function

---

## 8. Development & Future Plans

* **Languages**: Markdown, JSON
* **Environments**: ChatGPT Canvas, Notion
* **Testing**: GPT-4o, Gemini 2.5 Flash
* **Publishing**: GitHub Pages (v1.3)

### Roadmap

* API for syntax generation and conversion
* Dictionary linking modifiers to natural language impressions
* Standardization of emotion tokens across multimodal models

---

© 2025 Yui & Yuu – Released under a non-commercial license.
