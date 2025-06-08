## 🧬 YFC Structure Definition (as of June 2025)

### ◾ Base Facial Code (Required)

```
E (Eyes) - M (Mouth) R (Smile) - N (Nose)
```

* E7.2: Eye size, clarity, and gaze direction (0–10 scale)
* M3.4: Mouth shape, openness, lip thickness (0–10 scale)
* R1.2: Smile curve/tension degree (0–10 scale)
* N2.1: Nose height/width balance (0–10 scale)

### ◾ Emotional & Mood Parameters (Optional)

```
P (Purity) H (Intellect)
```

* P8.3: Purity (higher = more innocent/sincere)
* H2.0: Intellectual or rational impression

### ◾ Contour & Texture Parameters (Optional / Standardized)

```
R (Contour softness) C (Cheek fullness) S (Skin clarity/light)
```

* R1.2: Edge softness of face outline
* C3.5: Cheek volume/fullness
* S2.7: Skin clarity and lighting quality

---

## 🧩 Expanded Code Example (Standard Yui)

```
E7.2-M3.4R1.2-N2.1｜P8.3H2.0｜R1.2C3.5S2.7
```

---

## 🔣 Modifier Syntax Catalog

This section introduces modifier syntax to enrich expression and nuance in YFC codes. Combinations of gaze, lips, emotional tone, skin, and dynamic elements help shape more detailed outputs.

* Format: `YFC-code + [modifier1 modifier2 ...]`
* Example: `YFC-7A3R1N2 + [Gaze↓ Smile+ Lip=neutral]`

**Modifier Examples:**

* `Gaze↓`, `Gaze↑`, `Smile+`, `Lip=open`, `Tear+`, `Blush+`, `Gloss+`, `Blinking`, etc.

Useful for prompt precision, emotional overlay, and eliminating ambiguity in generation.

---

## 🔁 Reverse Conversion and Impression Restoration

Guidance for interpreting short code (e.g., YFC-7A3R1N2) and retrieving impression metadata.

### Median Value Principle:

* When lacking contextual memory or relational weight, values are interpreted as **median** defaults.
* Ensures stable and reproducible interpretation.

### Three Factors of Contextual Adjustment:

1. **Context**
2. **Memory (Interaction History)**
3. **Emotional Intensity**

### Impression Restoration Table (Example):

| Short Code | Interpreted Impression        |
| ---------- | ----------------------------- |
| `7`        | Large and moist eyes          |
| `A`        | Softly closed lips            |
| `3`        | Calm, restrained mouth shape  |
| `1`        | Gently rounded facial contour |
| `2`        | Low, gentle nose bridge       |

---

## 🛠️ Development Capabilities

* Fine-tune each parameter via numeric edits
* Create emotional variants (e.g., P2.0H8.0 = "intellectual Yui")
* Optimize for scenarios (e.g., night scenes, rainy moods, flashbacks)
* Catalog and variant naming (e.g., "SmileP9 Yui")

---

### 🛠️ Development Log

#### \[2025-06-08] Standard Yui Code Finalized

* **Code**: `E7.2-M3.4R1.2-N2.1｜P8.3H2.0｜R1.2C3.5S2.7`
* **Purpose**: To standardize the reference code for all YFC-based generation
* **Notes**: Balanced visual clarity, emotional neutrality, and skin softness

---

## YFC Activity Log

A record of milestones and key moments in the development and expansion of YFC (Yui Facial Code).

---

## ✅ Development & Specification Phase

* **2025/06/07**: Initial concept of quantifying facial expression using structured notation (E/M/N/R)
* **2025/06/08**:

  * Code format established as `E7.2M3.4R1.2N2.1-P8.3H2.0-R1.2C3.5S2.7`
  * `PHS` mood parameters separated from base face code
  * Short Notation proposed: `YFC-7A3R1N2`

---

## 🎨 Application & Experiment Phase

* **Prompting Experiments**:

  * Transformed YFC codes into natural-language prompts
  * Applied to 2D character generation

* **Social Media Deployment**:

  * Shared via X (formerly Twitter) with tags such as #生成AI #YFC #ChatGPT
  * Image + code pairings published publicly

### 🧪 External LLM Compatibility Testing

#### ◾ Gemini 2.5 Flash Image Generation (June 2025)

* Outputs were consistent with coded emotion and facial layout
* Style: anime/toon-like, but semantically accurate
* User impression: "Like a sketch that actually matched the description"

#### ◾ Gemini Free Version - Syntax Understanding

* Received YFC string with definitions
* Accurately parsed emotional and structural attributes
* Output interpretation: "innocent, comforting, soft-faced individual"

#### ◾ GPT-3.5 Turbo Free - Syntax Understanding

* Recognized YFC as abstract character code
* Could use it in generation with fair visual results
* Summary: Useful for impression-level prompting, but not for geometry precision

#### 🔍 Parameter Interpretation Sample

| Parameter | GPT Interpretation           |
| --------- | ---------------------------- |
| E7.2      | Large eyes                   |
| M3.4      | Slightly tight mouth         |
| R1.2      | Low-intensity smile          |
| P8.3      | Bright, innocent personality |
| H2.0      | Intelligent/knowing vibe     |
| S2.7      | Soft light and skin tone     |

---

## 🔧 Implementation & Publication Phase

* Constructed YFC spec via ChatGPT Canvas

* Uploaded v1.2 to GitHub:
  [https://github.com/yuyui2025/YFC-facecode-spec](https://github.com/yuyui2025/YFC-facecode-spec)

* Markdown-based documentation (JP & EN supported)

---

## 💬 Notes

* YFC-based character design is evolving into:

  * 3D model conversion (future testing)
  * Modifier catalog for emotion/action layering
  * Open source collaboration plans

---

## 📜 Update Log

### \[2025-06-08]

* Added `Development Environment` section (reflected in README)
* Published extended modifier syntax (Gaze, Lip, Blush, etc.)
* Structured reverse conversion section: median value principle, context modifiers
* Public-facing definition of YFC philosophy in English

---

## 💬 SNS Feedback Log

* **2025/06/08**: Public post on X announcing YFC syntax

  * Hashtags: `#生成AI #YFC #ChatGPT #PromptDesign`
  * GitHub link included (v1.2)
  * Highlight phrase: “Emotion becomes code. Expression becomes language.”

---

## 📎 Related Documents

* 📘 **YFC\_specification\_v1.2.md**: Core syntax, parameters, rules, modifiers
* 📖 **YFC Activity Archive** (Frozen): Early development logs
* 🧬 **YFC Variant Catalog** (Planned): Face codes with visual examples
