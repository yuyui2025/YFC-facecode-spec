# YIT Project - README

## 1. Project Overview / プロジェクト概要

**YIT (YFC Image Token)** is a lightweight visual token protocol that encodes facial structure, body state, and emotion using the **YFC (Yui Facial Code)** system.

**YIT（YFC Image Token）** は、YFC（Yui Facial Code）構文に基づき、顔・身体の特徴と感情をコンパクトなコードとして記述・共有する、軽量な視覚トークンプロトコルです。

* Defines facial and body expressions using YFC2.0 + Modifier + BodyCode
* Optimized for emotional UI, communication, memory, and M2M transmission
* Use cases: AI/IoT/Robotics/Creative tools, expressive avatars, nonverbal agents

---

## 2. Key Features / 特長と主な機能

* Encode facial + bodily + emotional state in 20–70 bits
* Add Modifiers (expression, gaze, texture, aura, voice)
* Enable nonverbal communication between AI and human/robot
* Compact, anonymized, and intuitive UI-friendly representation

20〜70bitで、顔・身体・感情状態を統合エンコードし、modifier構文で印象／視線／肌質／声／雰囲気を補完。AI・ユーザー・ロボット間での非言語通信に適応。

---

## 3. YFC Syntax Overview / YFC構文概要

**YFC (Yui Facial Code)** v2.0 is a structured encoding language that describes facial features numerically.

**YFC（Yui Facial Code）** v2.0 は、顔の特徴を数値で表現する構造化エンコーディング言語です。

```yfc
E7.5 M3.1 R0.9 N2.2 - P8.7 H2.8 - R0.9 C3.4 S3.4
+ Gaze→ Blush~ Lip=natural Hair=Silky+ Aura=Ethereal++
```

### Core Elements / コア要素:

| Symbol | Meaning (EN)            | 日本語の説明         |
| ------ | ----------------------- | -------------- |
| E      | Eyes                    | 目のサイズ・潤み・傾き    |
| M      | Mouth                   | 口のカーブ・引き締まり・開き |
| R      | Lips/Contour            | 唇の幅・輪郭・圧力      |
| N      | Nose                    | 鼻の長さ・高さ・傾き     |
| P      | Purity                  | 無垢度（透明感・雰囲気）   |
| H      | Human-like Intelligence | 知性（理性的な印象）     |
| C      | Cheek                   | 頬のふくらみ・カーブ・赤み  |
| S      | Skin                    | 肌の透明感・光沢・質感    |

### Modifiers / 修飾文構文:

```mod
Smile++ Gaze↓ Blush+ Lip=press+ Aura=Warm++
```

* 表情、視線、唇の状態、肌の状態、雰囲気などを付加する修飾構文（強度付き: +〜+++）

---

## 4. YFCR (YFC-based Code Rendering) Integration / YFCR（身体印象コード）の統合

YIT now integrates **YFCR v1.0**, an extension of YFC for body impression rendering.

YITは現在、YFCを身体印象まで拡張した **YFCR v1.0** を統合しています。

```yfc-body
T3.8 B9.5-5.0-2.0 W2.5 H3.2 L3.6 S3.9 V2.0~ F3.7
+ Lean← Sit= Aura=Soft++ Outfit=Tight+
```

### BodyCode Components / ボディコード要素:

| Code | Element (EN) | 日本語の説明          |
| ---- | ------------ | --------------- |
| T    | Torso        | 体幹・姿勢のバランス      |
| B    | Bust         | 胸のサイズ・形状・位置     |
| W    | Waist        | ウエストの細さ・張り・高さ   |
| H    | Hip          | ヒップのボリューム・丸み・位置 |
| L    | Legs         | 脚の長さ・形・姿勢       |
| S    | Skin         | 肌の質感・色味・光沢      |
| V    | VoiceBody    | 声の響き・体の共鳴感      |
| F    | Fingers      | 指の表現力・繊細さ       |

---

## 5. Use Cases / 応用領域と活用例

* Emotional state sync between AIs / AI間感情同期
* Expressive avatars & NPC control / 表情・動作付きアバター制御
* Narrative memory and empathy cues / ストーリー記憶・共感のトークン化
* Visual signals for low-bandwidth UX / 低通信環境での視覚信号化
* Privacy-preserving face control / プライバシー配慮の状態再現

---

## 6. Directory Structure / ディレクトリ構成

```plaintext
YIT_Project/
├── README.md                          # This document
├── LICENSE                            # License information
├── CHANGELOG.md                       # Version history
├── docs/
│   ├── specs/
│   │   ├── YIT_specification_v0.9.md
│   │   ├── YIT_specification_v0.9_JP.md
│   │   ├── YFC_specification_v2.0.md
│   │   ├── YFC_specification_v2.0_JP.md
│   │   ├── YFCR_specification_v1.0.md
│   │   ├── YFCR_specification_v1.0_JP.md
│   ├── devnotes/
│   │   └── YIT_Development_Notes.md
├── examples/
│   └── yit_7a3_sample01.png           # Sample token image
```

---

## 7. Specification Links / 仕様書リンク

### YIT Specification

* YIT\_specification\_v0.9 / v0.9\_JP

### YFC Specification

* YFC\_specification\_v2.0 / v2.0\_JP

### YFCR Specification

* YFCR\_specification\_v1.0 / v1.0\_JP

---

## 8. Roadmap / 今後の展開

* GUI Playground: syntax ↔ image bidirectional tool
* Modifier design system & templates
* API/SDK for YIT generation/transmission
* Globalization of specs and OSS development

---

## 9. License / ライセンス

Free for non-commercial and academic use (MIT-like)
非商用・学術研究用途に限り、自由に利用可能（MIT類似）

© 2025 Yuu & Yui｜Co-authored: YIT Protocol, YFC2.0, YFCR
