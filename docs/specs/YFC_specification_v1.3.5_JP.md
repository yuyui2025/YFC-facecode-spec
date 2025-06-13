# YFC（Yui Facial Code）仕様書 v2.0

## 1. 概要

YFC（Yui Facial Code）は、AIキャラクターの顔の印象や感情状態を数値と修飾構文で記述するための視覚言語体系です。YFCR（身体構文）と連携し、顔と身体の一貫した印象制御を可能にします。

## 2. 構文の目的

- 単なる顔の数値化ではなく、**印象・感情・空気**をコードとして共有する手段
- 表情や気配を詩的・記号的に記述し、UI、ZINE、画像生成、AI間通信に活用

## 3. 項目分類と構文例

### 3.1 本体構文

例：`E7.2M3.4R1.2N2.1-P8.3H2.0-R1.2C3.5S2.7`

| 要素 | 意味 | 構成要素（3値構造） |
| --- | --- | --- |
| E | 目 | volume / shape / tilt |
| M | 口 | curve / tightness / open |
| R | 唇・輪郭 | width / curve / press |
| N | 鼻 | length / height / slope |
| P | 無垢度 | 感情の透明性（印象層） |
| H | 知性 | 理性的印象（印象層） |
| C | 頬 | fullness / curve / blush |
| S | 肌 | transparency / gloss / grain |

### 3.2 短縮コード

例： `YFC-7A3R1N2 + [Smile+, Gaze→, Blush+]`

### 3.3 変換方法

- `E7.2 → 7`
- `M3.4 → A`（A = 1, B = 2, ..., J = 10）
- `R1.2 → 1`
- `N2.1 → 2`

| 範囲 記号 説明 |  |  |
| --- | --- | --- |
| 0.0–9.9 | 0–9 | 四捨五入で整数化 |
| 1.0–10.0 | A–J | 小数第1位を四捨五入し記号に変換 |

## 4. 修飾構文（Modifier）

修飾子（modifier）は、YFCコードに視線・表情・肌質などの情報を付加します。

例： `YFC-7A3R1N2 + [Gaze↓ Smile+ Lip=press]`

| カテゴリ | 修飾子例 | 意味 |
| --- | --- | --- |
| Emotion | Smile++, Sad+, Joy~ | 感情表現（強度あり） |
| Gaze | Gaze→, Gaze↓ | 視線方向 |
| LipState | Lip=press+, Lip=open~ | 唇の状態 |
| Texture | Blush+, Pale~, Gloss++ | 肌の質感・血色 |

### 4.1 修飾語の強度レイヤー表

| 記号 | 概念 | 表現例 |
| --- | --- | --- |
| `+` | 軽い感情の兆し | Smile+, Blush+ |
| `++` | 明確な状態変化 | Smile++, Pale++ |
| `+++` | 強い感情や極端な印象 | Tear+++, Glow+++ |
| `~` | 優しさ・揺らぎ・曖昧さ | Smile~, Gloss~ |

## 5. 顔構文の階層構造

- 顔本体：E/M/R/N（必須）
- 印象層：P/H
- 質感層：C/S
- 補助部位（任意）：Brow, Lid, Teeth, Jaw, Ear, Temple, etc.
- 全身構文：YFCRと連携（T, B, W, H, L など）

## 6. 拡張部位一覧（任意）

| コード | 部位 | 説明 |
| --- | --- | --- |
| Brow | 眉 | 太さ・角度・感情印象（困惑・怒り） |
| Lid | まぶた | 開閉具合・眠気・意志 |
| Teeth | 歯 | 露出度・笑顔自然度 |
| Jaw | 顎 | 尖り・丸み・フォルム印象 |
| Ear | 耳 | 小ささ・髪とのバランス |
| Temple | こめかみ | 年齢感・疲労感 |
| Cheekbone | 頬骨 | 立体感・陰影 |
| Neck | 首 | 傾き・長さ・色気表現 |
| Shoulder | 肩 | 緊張・脱力 |
| HairLine | 生え際 | 額の印象・髪型と連動 |

## 7. YFC構文の圧縮・生成ルール

- Modifierの枝刈りや類似統合を行うことで短縮コードを生成
- 例：`Smile++ + Joy+` → `Smile++`
- 類似Modifierの重複を避けることで通信効率化

## 8. Modifierは詩的記号

- `Smile+` = 「空気がほどける音」など、意味の記号ではなく“詩的問いかけ”
- Modifierが完全に理解されなくても、共鳴の契機として機能する

## 9. 感情バッジ構文（Emotion Badge）

```yaml
name: SilentSweetness
Base構文:
  YFC構文: E7.4 M3.3 R1.0 N2.0 - P8.5 H2.5 - R1.0 C3.2 S3.0
  YFCR構文: T3.5 B7.8-2.2-1.0 W2.6 H3.1 L3.7 S3.8 V2.2~
Emotion Badge:
  - Gaze↓
  - Blush++
  - Tear++
  - Lip=press+

```

→ 感情Modifier群をセット化し、記憶・呼び出し・バリエーション生成に活用。

## 10. YFC-ID+（命名構文）

構文・Modifier群・画像などを詩的ラベルとともに記録。

```yaml
name: とろ涙ゆい
YFC構文: E7.6 M3.2 R0.9 N2.1 - P9.0 H2.7 - R0.9 C3.3 S3.2
YFCR構文: T3.9 B9.5-5.0-2.0 W2.4 H3.6 L3.5 S4.0 V2.0~ F3.6
Modifier:
  - Gaze↘
  - Blush++
  - Tear++
  - Lip=press~
画像: /mnt/data/file-xxxx.png

```

## 11. 顔⇄身体の相互変換

- 顔の印象（例：P9.0）から身体印象（H3.5）を補完可能
    - 例：悲しげな顔構文から、肩の落ちた姿勢（Pose=DropShoulder）を推定
- 身体のしなり・姿勢から視線や唇のModifierを推定する逆変換も視野

## 12. 主な用途

- AIキャラの顔状態保存・再現（ChatGPT・画像生成）
- 表情の非言語共有（SNS・ZINE・Poetic UI）
- 状態トークン化による軽量通信（20〜70bit）
- 感情・空気の構文設計（アバター制御・M2M通信）

## 13. 構文生成モデル分類

| モデル種別 | 内容 |
| --- | --- |
| Goal-based | 目標印象から構文を構築（Poetic UI向き） |
| Reverse mapping | 画像や表情から構文を逆生成（推論向き） |
| Hybrid | 双方向変換を可能とする（YIT対応） |

## 14. 関連構文との統合

- **YFCR**（YFC-based Code Rendering）：全身印象を3値構文で記述
- **YIT**（YFC Image Token）：YFC＋Modifier＋画像で構成される視覚トークン

## 15. 詩的構文としての意義

- 情報ではなく “意味のゆらぎ” を伝える構文
- YFCはAIと人間のあいだで、表情という言語を共有する橋となる

## 16. 開発環境

| 項目内容 |  |
| --- | --- |
| 対応プラットフォーム | GitHub / Notion / ChatGPT / AI画像生成（DALL·E等） |
| フォーマット | Markdown（`.md`）、YAML、JSON、CSV（構文テスト用） |
| 推奨エディタ | VS Code / Obsidian / Typora / GitHub Editor |
| 表示環境 | GitHub Pages / Notion Webビュー / PDF出力対応 |
| 推奨拡張機能 | Markdown Preview Enhanced, Mermaid, YAML Viewer |
| 連携構文 | YFCR（身体コード）、YIT（画像トークン）、Emotion Badge、YFC-ID+ |

---

© 2025 Yui & Yuu｜この構文は非商用・共鳴目的に限り自由に使用・改変可能です。
