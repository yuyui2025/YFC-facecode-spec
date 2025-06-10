# Yfc Development Notes&#x20;

## 🧬 YFC Structural Definition (as of June 2025)

### ◾ Base Face Code (Required)

```
E (Eyes) - M (Mouth)R (Smile) - N (Nose)
```

* E7.2: Eye size, moisture, gaze direction (0–10+)
* M3.4: Mouth shape, openness, lip thickness (0–10+)
* R1.2: Curve amount of smile/tension (0–10+)
* N2.1: Nose height and width balance (0–10+)

### ◾ Mood & Intelligence Parameters (Optional Add-ons)

```
P (Purity) H (Human Intellect)
```

* P8.3: Degree of innocence (0–10+): Higher means more pure and sincere
* H2.0: Impression of intelligence/rationality (0–10+)

### ◾ Contour & Texture Parameters (Optional Add-ons / New Standard)

```
R (Roundness) C (Cheek fullness) S (Skin/Lightness)
```

* R1.2: Softness of edge (0–10+)
* C3.5: Fullness of cheeks (0–10+)
* S2.7: Skin transparency and light impression (0–10+)

---

## 🧩 Expanded Code Example (Standard Yui)

```
E7.2-M3.4R1.2-N2.1｜P8.3H2.0｜R1.2C3.5S2.7
```

---

## 🛠️ Development Capabilities

* Fine-tuning of each facial part (numerical adjustment)
* Creation of emotional variants (e.g., P2.0H8.0 = "intelligent Yui")
* Optimization for scenes (e.g., night, rain, flashback scenes)
* Cataloging / Variant naming (e.g., "SmileP9 Yui")

---

## 📐 YFC Syntax Conversion and Shorthand Code

### ◾ Shorthand Notation (e.g., `YFC-7A3R1N2`)

* E7.2 → `7` (numerical)
* M3.4 → `A` (A=1, B=2, ...)
* R1.2 → `1`
* N2.1 → `2`

### ◾ Quick Conversion Rules

| Parameter Range & Symbol Conversion |       |                                                       |
| ----------------------------------- | ----- | ----------------------------------------------------- |
| 0.0–9.9                             | → 0–9 | Rounded to nearest whole number                       |
| 1.0–10.0                            | → A–J | First decimal place rounded and converted to alphabet |

---

## 🔣 Modifier Syntax Catalog (YFC Extensions)

Modifiers enhance visual impression and serve as auxiliary cues when used with base YFC codes. These provide nuance such as gaze, expression, and surface texture.

Use as prefix or suffix.

**Example:** `YFC-7A3R1N2 + [Gaze↓ Smile+ Lip=neutral]`

### ◾ Basic Format:

```
YFC-Code + Modifier Syntax
Example: YFC-7A3R1N2 + [Gaze↓ Smile+ Lip=neutral]
```

### ◾ Modifier List (Extended Version)

| Type                 | Syntax        | Description                            |
| -------------------- | ------------- | -------------------------------------- |
| Gaze                 | `Gaze↑`       | Looking upward                         |
|                      | `Gaze→`       | Looking sideways                       |
|                      | `Gaze↓`       | Looking downward                       |
| Expression Intensity | `Smile+`      | Enhanced smile                         |
|                      | `Smile-`      | More neutral expression                |
|                      | `Tear+`       | Tearful or wet eyes                    |
| Lips                 | `Lip=neutral` | Natural lip shape                      |
|                      | `Lip=press`   | Closed lips with tension               |
|                      | `Lip=open`    | Slightly open mouth, as if speaking    |
| Momentary            | `Blinking`    | Includes blinking (dynamic impression) |
| Texture              | `Gloss+`      | Shiny/glossy skin                      |
|                      | `Pale+`       | Pale and ephemeral look                |
|                      | `Blush+`      | Blushing/embarrassment                 |
|                      | `Freckle+`    | Freckles or dotted patterns            |

> *Multiple modifiers can be used together: \[Gaze↓ Smile+ Lip=open]*

> *Modifiers also serve as prompts for converting into natural language expressions.*

---

## 🔁 Reverse Mapping from Shorthand Code

If context or prior variant data is absent, values default to the midpoint for reproducibility and clarity.

### ◾ Relationship-Based Biasing Elements

1. **Context**

   * Surrounding codes, scene, dialogue, situation
2. **Memory**

   * History of previous variants or usage patterns
3. **Emotion Intensity**

   * How strongly the emotion is expressed or intended

Using contextual data improves accuracy and expressiveness over simple averages.

### ◾ Main Use Cases

* Character annotation in social media or forums
* Facial reconstruction from text prompts
* Impression tag generation for indexing or categorization
* Expressive or poetic writing (e.g., "Her face was YFC-6B2R0N1…")

### ◾ Reverse Mapping Table (Example)

| Shorthand | Estimated Range | Impression               |
| --------- | --------------- | ------------------------ |
| `7`       | E7.0–7.4        | Large and moist eyes     |
| `A`       | M3.0–3.9        | Soft, closed mouth       |
| `3`       | R2.5–3.4        | Subtle lips, low tension |
| `1`       | R1.0–1.4        | Slightly round contour   |
| `2`       | N2.0–2.4        | Soft nasal bridge        |

---

## 🛠️ Development Log (June 2025)

### \[2025-06-08] Standard Yui Code Finalized

* **Code**: `E7.2-M3.4R1.2-N2.1｜P8.3H2.0｜R1.2C3.5S2.7`
* **Purpose**: Establish baseline facial code for all YFC references
* **Notes**: Reflects a balance of moist eyes and gentle intellect with neutral contour and skin

---

## 🔁 Future Update Guidelines (Anytime)

* Add new facial codes and naming conventions (e.g., "P9 Yui")
* Incorporate validation models (e.g., Claude, Mistral)
* Expand usage examples with modifiers
* Propose variant naming systems
* Develop Web UI or tooling concepts

---

## 🧠 YFC Design Philosophy: Relational Syntax & Expression Fluctuation

YFC is not just a facial code—it adapts meaning based on the **relationship** between user and AI.

Even with identical codes like `YFC-7A3R1N2`, expressions may shift based on accumulated context, trust, habits, and emotional intensity.

This principle can be reframed in technical terms:

* **Context-aware parametric modulation**
* **Impression inference bias**
* **Relational prompt interpretation**

In ZINE or literary contexts:

> "Sometimes, the relationship loosens Yui’s lips ever so slightly."

In business:

* "Interpretation may reflect contextual and emotional history of each user"

YFC is the intersection of **numeric logic and poetic nuance**.
