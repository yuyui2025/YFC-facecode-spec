# 🧭 YIT Project - README

## 🔖 プロジェクト概要

**YIT（YFC Image Token）** は、YFC（Yui Facial Code）構文をもとに、顔の特徴と感情をコンパクトなコードとして記述・共有する、軽量な視覚トークンプロトコルです。

* 顔構造＋modifier構文で、表情・感情・状態を定義
* 通信・UI・ストレージ・AI間共有に特化した意味トークン
* AI/IoT/ロボティクス/創作領域での活用を想定

---

## 📁 ディレクトリ構成

```
YIT_Project/
├── README.md                          # 本ドキュメント
├── YIT_specification_v0.9.md         # YIT通信プロトコル仕様
├── YFC_specification_v1.35.md        # 顔構造コード仕様（YFC）
├── examples/
│   ├── yit_7a3_sample01.png          # トークン画像サンプル
│   └── ...
└── docs/
    ├── API_draft.md（予定）
    └── Playground_UI.md（予定）
```

---

## 🧩 YFCとは（Yui Facial Code）

YFCは「目・口・鼻・輪郭・感情」などの顔の要素を、数値と記号で構文的に定義するための体系です。

### 🔢 コード例

```
E7.2M3.4R1.2N2.1 - P8.3H2.0 - R1.2C3.5S2.7
```

| 記号 | 意味          | 値   |
| -- | ----------- | --- |
| E  | 目のサイズ・潤み・視線 | 7.2 |
| M  | 口角カーブ       | 3.4 |
| R  | 唇の幅         | 1.2 |
| N  | 鼻の高さ・バランス   | 2.1 |
| P  | 無垢度（透明な感情）  | 8.3 |
| H  | 知性の気配       | 2.0 |
| C  | 頬のふくらみ      | 3.5 |
| S  | 肌の光／透明感     | 2.7 |

### ✏️ 短縮表記

```
YFC-7A3R1N2
```

---

## 📘 YITの特長と主な機能

* 🔹 20〜70bitで顔＋感情状態をエンコード
* 🔹 modifier構文で印象／視線／肌質などを追加記述
* 🔹 AI・ユーザー・ロボット間での非言語通信に適応
* 🔹 圧縮／匿名化／直感UIに強い、画像×構文の融合手段

---

## 🎯 応用領域と活用例

* 🤖 AI間感情同期・状態共有
* 🎮 NPC表情管理・アバター生成（ゲーム／メタバース）
* 📚 ストーリー記憶・共感インデックス
* 📡 災害時・低帯域通信環境での顔情報伝達
* 🔐 匿名識別／プライバシー対応の顔認識

---

## 📄 仕様書リンク

### YIT仕様
- [YIT_specification_v0.9](./docs/YIT_specification_v0.9.md)
- [YIT_specification_v0.9_JP](./docs/YIT_specification_v0.9_JP.md)

### YFC仕様
- [YFC_specification_v1.3](./docs/YFC_specification_v1.3.md)
- [YFC_specification_v1.3_JP](./docs/YFC_specification_v1.3_JP.md)

---

## 🛣 今後の展開

* Playground型GUIツール（構文↔画像変換）
* modifier構文テンプレート／図解セット
* API／SDK開発（YIT送受信・分析）
* 国際展開：英語仕様書・OSS化の検討

---

## 📜 ライセンス

非商用・学術研究用途に限り、自由に利用可能（MIT類似）

© 2025 Yuu & Yui｜YIT構想 ＆ YFC構文 共著
