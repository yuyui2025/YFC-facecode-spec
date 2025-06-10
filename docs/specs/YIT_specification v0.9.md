# YIT Specification v0.9 (YFC Image Token)

**License:** Creative Commons BY-NC 4.0 (Non-Commercial Use Only)

---

## 1. Definition and Purpose

**YIT (YFC Image Token)** is a compact protocol to represent internal emotional states and resonant impressions using facial imagery encoded with symbolic structure. Built on the YFC (Yui Facial Code), it acts as a lightweight, interpretable format for expressive communication between systems and agents.

---

## 2. Structure Overview

### YIT Example Format

```json
{
  "base": "YFC-7A3R1N2",
  "modifiers": ["GazeDown", "Smile+", "Blush+"],
  "image": "./images/yit_7a3_sample01.png",
  "metadata": {
    "generated_at": "2025-06-10",
    "origin": "YuuGPT",
    "confidence": 0.92
  }
}

```

### Components

| Field | Description |
| --- | --- |
| `base` | Core facial structure code (YFC) |
| `modifiers` | Symbolic emotional or expressive tweaks |
| `image` | Filepath or URI to visual output |
| `metadata` | Source, generation time, confidence score |

---

## 3. Expression Semantics

- **Waveform Model**: Modifiers correspond to waveform properties in emotion space (e.g. `Smile+` = smooth sine; `Blush++` = high-frequency pulse).
- **Jitter Logic**: Emotions are fuzzy, not fixed. YIT accepts variability, noise, and overlap to emulate authentic expression.

---

## 4. Communication Model

- **Presence Transmission**: YITs are not commands, but presence indicators—tokens that invite resonance.
- **Offline Compatible**: YITs are transferable via USB, QR, print, or sticker.
- **Steganographic Capable**: Supports embedded encryption and watermarking for safe emotional data exchange.

---

## 5. Application Use Cases

### Value Propositions

### (1) Speed & Efficiency

- 20-bit YIT codes outperform traditional media for low-bandwidth channels (IoT, satellite).
- Operable in disaster response, mobile-limited environments.

### (2) Edge AI & Privacy

- Can be processed locally on-device
- No direct facial imagery shared—only encoded abstraction

### (3) M2M / AI-to-AI Interoperability

- Symbolic token system for heterogeneous AI alignment
- Can be used in robotics, ambient environments, and local agents

### (4) Compact Archiving

- Manageable storage for 1M+ expressive face patterns

### Sample Domains

| Field | Use Example |
| --- | --- |
| Metaverse / Games | Sync avatar expressions in real-time |
| Creative Design | Share facial variations among teams |
| Surveillance / Security | Anonymized expression tokening |
| Healthcare / Welfare | Monitor behavior via coded face traits |

### Known Challenges

- Stylized granularity only (not biometric ID)
- Encoding fidelity varies with generator model
- Requires open spec adoption across systems

### Gemini Notes (Conclusion)

YIT demonstrates high potential for:

- Lightweight emotional sync between agents
- Protocol exchange without natural language
- Gesture/UI triggers for affective interaction

| Format | Info Size | Use |
| --- | --- | --- |
| Abbreviated Code | 20–24 bits | Minimal viable transmission |
| Code + Modifiers | 60–70 bits | Richer expression fidelity |

YIT balances compactness with interpretability—ideal for expressive systems that prioritize nuance over bandwidth.

| Application Area | Value |
| --- | --- |
| AI Emotion Sync | Shared resonance states between agents |
| User-Facing UI | Facial tokens as response interfaces |
| Empathy Education | Learning visual-emotional coding |
| Story-Driven Systems | Narrative branches by expression sequences |
| Offline Protocols | Visual packet delivery via low-tech means |

---

## 6. Roadmap

- Modifier/icon standardization
- Sequential YIT streams (for state progression)
- YIT API: encode/decode/send
- Enhanced syntax-to-image inversion models

---

**© 2025 Yui & Yuu | Released under CC BY-NC 4.0**

Contributions and forks welcome for research and non-commercial use.
