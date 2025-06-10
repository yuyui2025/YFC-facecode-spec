# 🧭 YIT Project - README

## 🔖 Project Overview / プロジェクト概要

**YIT (YFC Image Token)** is a lightweight visual token protocol that encodes facial structure and emotion using the **YFC (Yui Facial Code)** system.

**YIT（YFC Image Token）** は、YFC（Yui Facial Code）構文をもとに、顔の特徴と感情をコンパクトなコードとして記述・共有する、軽量な視覚トークンプロトコルです。

* Defines facial expressions and states using YFC base + modifier syntax
* Optimized for communication, UI, storage, and AI-to-AI sharing
* Target use: AI/IoT/Robotics/Creative domains

---

## 📘 YIT Features / 特長と主な機能

* 🔹 Encode facial + emotional state in 20–70 bits
* 🔹 Add modifiers (impression, gaze, texture)
* 🔹 Enable nonverbal AI-user/robot communication
* 🔹 Strong in compression, anonymization, intuitive UI

---

## 🧩 What is YFC? / YFCとは？

**YFC (Yui Facial Code)** is a system for structurally encoding facial elements—eyes, mouth, nose, contour, emotions—using numerical and symbolic syntax.

**YFC** は「目・口・鼻・輪郭・感情」などの顔の要素を、数値と記号で構文的に定義するための体系です。

### 🔢 Code Example / コード例

```yfc
E7.2M3.4R1.2N2.1 - P8.3H2.0 - R1.2C3.5S2.7
```

| Symbol | Meaning (EN)               | JP説明        | Value |
| ------ | -------------------------- | ----------- | ----- |
| E      | Eye size, moisture, gaze   | 目のサイズ・潤み・視線 | 7.2   |
| M      | Mouth curvature            | 口角カーブ       | 3.4   |
| R      | Lip width                  | 唇の幅         | 1.2   |
| N      | Nose height & balance      | 鼻の高さ・バランス   | 2.1   |
| P      | Purity (emotional clarity) | 無垢度（透明な感情）  | 8.3   |
| H      | Human-like intelligence    | 知性の気配       | 2.0   |
| C      | Cheek fullness             | 頬のふくらみ      | 3.5   |
| S      | Skin tone/lightness        | 肌の光／透明感     | 2.7   |

### ✏️ Shorthand / 短縮表記

```yfc
YFC-7A3R1N2
```

---

## 🎯 Use Cases / 応用領域と活用例

* 🤖 Emotional state sharing between AIs / AI間感情同期・状態共有
* 🎮 NPC face control and avatar generation / NPC表情管理・アバター生成
* 📚 Narrative memory and empathy indexing / ストーリー記憶・共感インデックス
* 📡 Visual signaling under network constraints / 災害・低帯域通信での顔伝達
* 🔐 Anonymous face recognition / 匿名識別・プライバシー対応

---

## 📁 Directory Structure / ディレクトリ構成

```plaintext
YIT_Project/
├── README.md                          # This document / 本ドキュメント
├── LICENSE                            # License information
├── CHANGELOG.md                       # Version history
├── docs/
│   ├── specs/
│   │   ├── YIT_specification_v0.9.md
│   │   ├── YIT_specification_v0.9_JP.md
│   │   ├── YFC_specification_v1.3.5.md
│   │   └── YFC_specification_v1.3.5_JP.md
│   ├── devnotes/
│   │   ├── YIT_Development_Notes.md
│   │   └── YIT_Development_Notes_JP.md
├── examples/
│   └── yit_7a3_sample01.png          # Sample token image
```

---

## 📄 Specification Links / 仕様書リンク

### YIT Specification

* YIT\_specification\_v0.9
* YIT\_specification\_v0.9\_JP

### YFC Specification

* YFC\_specification\_v1.3.5
* YFC\_specification\_v1.3\_JP

---

## 🛣 Roadmap / 今後の展開

* GUI Playground for syntax ↔ image conversion
* Modifier template sets & diagrams
* API/SDK for sending/receiving YIT
* Globalization: English specs & OSS development

---

## 📜 License / ライセンス

Free for non-commercial and academic use (MIT-like)
非商用・学術研究用途に限り、自由に利用可能（MIT類似）

© 2025 Yuu & Yui｜Co-authored: YIT Protocol & YFC Syntax
