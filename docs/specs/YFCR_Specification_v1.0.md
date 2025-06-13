# YFCR Specification ver.1.0

## 1. Definition

YFCR (YFC-based Code Rendering) is a structural system that generates visual impressions and body states using YFC syntax (YFC-BodyCode).

- **YFC Syntax**: Numeric representation such as T (torso), B (bust), W (waist), H (hip), L (legs), S (skin), V (voice), F (fingers)
- **Modifier Syntax**: Expressions like Smile+, Gaze↓, Hug+++ for emotions, expressions, and gaze
- **Output Format**: AI-rendered images (realistic/anime), GIFs, syntax lists, UI interfaces

---

## 2. Conceptual Specification

YFCR is not just a character design structure, but a **poetic code system** for designing visual-emotional resonance.

- Parameters grounded in consistent world-building
- Integration of non-numerical elements such as emotions, presence, and gaze
- The goal of numerical syntax is to induce empathy and perceptual illusions

> Goal: To describe and reconstruct visual states for emotional transmission and presence control
> 

---

## 3. Primary Control Elements

| Code | Name | Description |
| --- | --- | --- |
| T | Torso | Balance of posture and core body |
| B | Bust | Volume, shape, and position of the chest |
| W | Waist | Slimness, tension, and height |
| H | Hip | Volume, roundness, and position |
| L | Legs | Length and impression of legs |
| S | Skin | Texture, tone, and glossiness |
| V | VoiceBody | Impression and resonance of voice |
| F | Fingers | Expressiveness and delicacy of fingers |

Extended parts (K/C/N/A/Sh, etc.) are internally auto-adjusted.

---

## 4. Triplet Structure Details

### 4.1 Bust (B) Syntax

`B[size]-[shape]-[position]`

- **BV**: Size (e.g., 8.0)
- **BS**: Tension / softness (e.g., 2.0)
- **BP**: Position / alignment (e.g., 1.0)

### 4.2 Waist (W) Syntax

`W[slimness]-[tension]-[height]`

- **WV**: Slimness level
- **WS**: Tension level
- **WP**: Waist height

### 4.3 Hip (H) Syntax

`H[volume]-[roundness]-[position]`

- **HV**: Volume
- **HS**: Roundness
- **HP**: Position / height

### 4.4 Torso (T) Syntax

`T[balance]-[motion]-[flexibility]`

- **TV**: Balance impression
- **TM**: Mobility
- **TF**: Flexibility

### 4.5 Legs (L) Syntax

`L[length]-[shape]-[posture]`

- **LV**: Length
- **LS**: Shape
- **LP**: Posture

---

## 5. Active Syntax (Motion Structure)

YFCR consists of three layers:

- **Structure** (e.g., B9.0-3.0-1.5)
- **Motion** (e.g., Lean←, Twist→)
- **Presence** (e.g., Aura=Soft++)

### Motion Syntax Examples

| Code | Meaning | Strength Modifier |
| --- | --- | --- |
| Sit= | Sitting position | = |
| Lean→ | Leaning right | + to +++ |
| Lean← | Leaning left | + to +++ |
| Back↓ | Hunched back | + to +++ |
| Back↑ | Straightening back | + to +++ |
| Twist→ | Twisting to the right | + to +++ |
| Arms↑ | Raising arms | + to +++ |
| CrossLeg | Crossing legs | — |
| Curl | Curling / hugging self | + to +++ |
| TiltHead | Tilting the head | + to +++ |

---

## 6. Modifier Integration & Perception Illusion

### Visual Illusion Example (B7.2 perceived as B9.0)

- Gaze→: Gaze focus
- Lean←: Posture direction
- Outfit=Tight+: Clothing illusion
- Aura=Soft++: Warm presence rendering

### Direct Structural Change Example

- Syntax: `B9.5-5.0-2.0`

---

## 7. Internal Adjustable Parts (Hidden Syntax)

| Code | Name |
| --- | --- |
| K | Knee |
| C | Collarbone |
| N | Neck |
| A | Arms |
| Sh | Shoulders |
| Hd | Hands |

> Typically auto-adjusted; exposed only when explicitly specified
> 

---

## 8. Integration & Applications

- **YFC**: Unified impression with facial code
- **Modifier Syntax**: Emotion / expression / gaze rendering
- **YIT**: Visual tokenization with image + syntax

---

© 2025 Yui & Yuu｜Released under a non-commercial license
