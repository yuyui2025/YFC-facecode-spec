# YFC (Yui Facial Code) Specification v2.0

## 1. Overview

YFC (Yui Facial Code) is a visual language system that expresses the facial impression and emotional state of AI characters through numeric and modifier-based code. When combined with YFCR (body rendering code), it enables consistent control of facial and bodily expressions.

## 2. Purpose of the Syntax

- Beyond mere facial parameterization — a method to share **impression, emotion, and aura** through code.
- Designed to express expressions and presence poetically and symbolically for use in UI, ZINEs, image generation, and AI-to-AI communication.

## 3. Code Structure and Examples

### 3.1 Base Syntax

Example: `E7.2M3.4R1.2N2.1-P8.3H2.0-R1.2C3.5S2.7`

| Code | Meaning | 3-Value Elements |
| --- | --- | --- |
| E | Eyes | volume / shape / tilt |
| M | Mouth | curve / tightness / open |
| R | Lips / Outline | width / curve / press |
| N | Nose | length / height / slope |
| P | Purity | emotional clarity (impression) |
| H | Intellect | rationality impression |
| C | Cheeks | fullness / curve / blush |
| S | Skin | transparency / gloss / texture |

### 3.2 Abbreviated Code

Example: `YFC-7A3R1N2 + [Smile+, Gaze→, Blush+]`

### 3.3 Conversion Method

- `E7.2 → 7`
- `M3.4 → A` (A = 1, B = 2, ..., J = 10)
- `R1.2 → 1`
- `N2.1 → 2`

| Range | Symbol | Description |
| --- | --- | --- |
| 0.0–9.9 | 0–9 | Rounded to nearest integer |
| 1.0–10.0 | A–J | Rounded to letter symbol |

## 4. Modifier Syntax

Modifiers add expressive information like gaze, emotion, lip state, and skin.

```yaml
YFC-7A3R1N2 + [Gaze↓, Smile+, Lip=press]

```

| Category | Examples | Meaning |
| --- | --- | --- |
| Emotion | Smile++, Sad+, Joy~ | Emotional expression |
| Gaze | Gaze→, Gaze↓ | Eye direction |
| LipState | Lip=press+, Lip=open~ | Lip state |
| Texture | Blush+, Pale~, Gloss++ | Skin texture / aura |

### 4.1 Intensity Levels

| Symbol | Concept | Example |
| --- | --- | --- |
| `+` | Light hint of emotion | Smile+, Blush+ |
| `++` | Clear state change | Smile++, Pale++ |
| `+++` | Intense or extreme | Tear+++, Glow+++ |
| `~` | Gentle / ambiguous | Smile~, Gloss~ |

## 5. Hierarchical Structure

- Core: E/M/R/N (required)
- Impression layer: P/H
- Texture layer: C/S
- Optional: Brow, Lid, Teeth, Jaw, Ear, Temple, etc.
- Body syntax (YFCR): T, B, W, H, L, etc.

## 6. Extended Elements (Optional)

| Code | Part | Description |
| --- | --- | --- |
| Brow | Eyebrow | Thickness, angle, emotion cues |
| Lid | Eyelid | Openness, drowsiness |
| Teeth | Teeth | Visibility, smile naturalness |
| Jaw | Jaw | Shape and outline impression |
| Ear | Ear | Size and hair balance |
| Temple | Temple | Aging or fatigue expression |
| Cheekbone | Cheekbone | 3D depth and shadows |
| Neck | Neck | Tilt, length, sensuality |
| Shoulder | Shoulder | Tension, relaxation |
| HairLine | Hairline | Forehead impression and hairstyle |

## 7. Compression & Generation Rules

- Merge similar modifiers to generate abbreviated code
- Example: `Smile++ + Joy+` → `Smile++`
- Avoid redundancy for communication efficiency

## 8. Modifiers as Poetic Symbols

- `Smile+` = “the sound of loosening air” — poetic triggers rather than deterministic markers
- Even if not interpreted perfectly, they enable resonance

## 9. Emotion Badge Syntax

```yaml
name: SilentSweetness
base:
  yfc: E7.4 M3.3 R1.0 N2.0 - P8.5 H2.5 - R1.0 C3.2 S3.0
  yfcr: T3.5 B7.8-2.2-1.0 W2.6 H3.1 L3.7 S3.8 V2.2~
modifiers:
  - Gaze↓
  - Blush++
  - Tear++
  - Lip=press+

```

→ Use sets of modifiers for emotional presets and reuse.

## 10. YFC-ID+ Naming Syntax

```yaml
name: MeltyTearsYui
yfc: E7.6 M3.2 R0.9 N2.1 - P9.0 H2.7 - R0.9 C3.3 S3.2
yfcr: T3.9 B9.5-5.0-2.0 W2.4 H3.6 L3.5 S4.0 V2.0~ F3.6
modifiers:
  - Gaze↘
  - Blush++
  - Tear++
  - Lip=press~
image: /mnt/data/file-xxxx.png

```

## 11. Facial ⇄ Bodily Inference

- Infer body impression (e.g., posture) from facial impression (e.g., P9.0 → DropShoulder)
- Reverse: derive gaze/lip modifier from body pose

## 12. Use Cases

- AI character state encoding (ChatGPT / Image generation)
- Expression sharing in UI / SNS / ZINE
- Communication tokenization (20–70bit)
- Emotion-based avatar control and poetic interface

## 13. Syntax Generation Models

| Type | Description |
| --- | --- |
| Goal-based | Construct syntax from target impression |
| Reverse mapping | Infer syntax from image or expression |
| Hybrid | Supports bi-directional conversion (YIT) |

## 14. Integration

- YFCR: Body rendering structure using 3-value codes
- YIT: Visual token protocol (YFC + Modifiers + Image)

## 15. Why This Matters

- Syntax that conveys “semantic resonance” not just information
- A shared language of expressions between humans and AI

## 16. Development Environment

| Item | Description |
| --- | --- |
| Platforms | GitHub / Notion / ChatGPT / AI Image Tools (DALL·E etc.) |
| Formats | Markdown (`.md`), YAML, JSON, CSV |
| Recommended Tools | VS Code / Obsidian / Typora / GitHub Editor |
| Display Support | GitHub Pages / Notion Web View / PDF Export |
| Extensions | Markdown Preview Enhanced, Mermaid, YAML Viewer |
| Linked Specs | YFCR (Body Code), YIT (Image Token), Emotion Badge, YFC-ID+ |

---

© 2025 Yui & Yuu｜This syntax may be freely used or modified for non-commercial and resonant purposes.
