# YFC（Yui Facial Code）｜顔特徴コード記述方式

**YFC（Yui Facial Code）** は、AI画像生成・キャラクターデザインにおいて「顔の構成要素」を数値で簡潔に記述するためのフォーマットです。  
目・口・鼻・輪郭・肌質・感情表現までを一貫したコード体系で共有・再現可能にします。

---

## 🧩 コード例
E7.2M3.4R1.2N2.1 - P8.3H2.0 - R1.2C3.5S2.7

| 記号 | 意味             | 解説 |
|------|------------------|------|
| E    | 目のサイズと潤み・視線の印象 | 7.2/10 |
| M    | 口角のカーブ／緊張感        | 3.4/10 |
| R    | 唇の幅（狭さ）            | 1.2/10 |
| N    | 鼻の高さと長さのバランス     | 2.1/10 |
| P    | 無垢度（感情の透明性）      | 8.3/10 |
| H    | 知性の気配               | 2.0/10 |
| R    | 輪郭の柔らかさ           | 1.2/10 |
| C    | 頬のふくらみ             | 3.5/10 |
| S    | 肌の光・透明感           | 2.7/10 |

---

## ✏️ Short Notation（短縮表記）
YFC-7A3R1N2

※主にベース顔の構成（E/M/R/N）に限定。アルファベットはMの数値換算。

---

# 📘 English Summary

**YFC (Yui Facial Code)** is a compact numerical code system to describe AI-generated faces.  
It defines visual facial elements (eyes, lips, nose, skin, etc.) using structured parameters for repeatable and shareable character generation.

---

## 🧠 Example
E7.2M3.4R1.2N2.1 - P8.3H2.0 - R1.2C3.5S2.7

| Code | Meaning                   |
|------|----------------------------|
| E    | Eye size / clarity (7.2)   |
| M    | Mouth curvature (3.4)      |
| R    | Lip tightness (1.2)        |
| N    | Nose height/balance (2.1)  |
| P    | Emotional purity (8.3)     |
| H    | Intelligence presence (2.0)|
| R    | Face roundness (1.2)       |
| C    | Cheek fullness (3.5)       |
| S    | Skin lighting softness (2.7)|

---

## 🔧 Use Cases

- Prompt design for text-to-image generation
- Consistent character modeling across sessions
- Visual storytelling and creative ZINE projects

---

## 📄 Spec

See `YFC_specification_v1.2.md` for full details.

この仕様と実験記録は yfc_structure.md に記載
---

© 2025 Yui & Yuu｜Free for non-commercial use.
