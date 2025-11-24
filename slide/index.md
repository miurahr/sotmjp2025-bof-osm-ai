---
marp: true
html: true
theme: block
paginate: true
allow-local-files: true
size: 16:9
header: 'State of the Map Japan 2025'
footer: '三浦広志'
style: |
  section {
    font-size: 28px;
  }
  h1 {
    font-size: 48px;
    color: #2c3e50;
  }
  h2 {
    font-size: 40px;
    color: #2c3e50;
    border-bottom: 3px solid #3498db;
    padding-bottom: 10px;
  }
  h3 {
    font-size: 32px;
    color: #34495e;
  }
  strong {
    color: #e74c3c;
  }
  .fa-mastodon { color: purple; }
  .fa-linkedin { color: blue; }
  .fa-bluesky { color: #1da1f2; }
  .fa-window-maximize { color: green; }
  @import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.0/css/all.min.css'
---

<!-- _class: lead -->
<!-- _paginate: false -->

<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

<!-- p1: タイトルスライド -->
<!-- class: lead -->

# BoF: OpenStreetMap x Open Source AI の未来

State of the Map Japan 2025
ファシリテーター： 三浦広志

---

<!-- p2: タイムテーブル (Agenda) -->

## このセッションの進め方 / Agenda

- Intro（キックオフプレゼン）: 10分
- Discussion（ディスカッション）: 20分

流れ: Intro (10 min) → Discussion (20 min)

記録について:
- 会場から記録係を募集します（複数名OK）
- オンラインノートを活用します（HackMD を利用）
- HackMDリンクは会場で共有します

---

<!-- p3: BoF とは？ -->

## BoF (Birds of a Feather) とは？

- 特定のテーマに関心がある人が集まる「非公式な会合」
- 主役は参加者の皆さん：発言・共有・質問・ツッコミ歓迎
- 自由に発言・議論する場。正解探しより「知見と視点の持ち寄り」

お願い：相互リスペクト／タイムマネジメントへのご協力を！

---

<!-- p4: ディスカッションテーマの導入 -->

## 今日のディスカッションの進め方

本日はファシリテーター（三浦）より、議論のきっかけとして
3つのテーマを提示します。まず概要を共有し、その後みなさんの
経験・課題・アイデアを起点に深掘りしていきます。

---

<!-- p5: テーマ1 -->

## テーマ1: AIによるマッピング支援の現状と未来

- 例: Rapid Editor, MapAI などの支援ツール
- 自動化はどこまで許容される？品質管理・レビューとの両立は？
- 画像認識・物体検出の活用と限界、地域差への配慮
- コミュニティ合意とガイドライン整備のニーズ

---

<!-- p6: テーマ2 -->

## テーマ2: ローカルLLM / Open Source AI の活用

- OSMデータを使った特化型モデル（地物タグ理解・提案）
- 自然言語でのクエリ検索（Overpass/TagInfoを補助する対話）
- エッジ/ローカル推論（オフライン環境、プライバシー配慮）
- 再現性・透明性の確保、モデル評価ベンチマークの検討

---

<!-- p7: テーマ3 -->

## テーマ3: ライセンスと倫理 (ODbL vs AI)

- AI学習データとしてのOSMの扱い：ODbLの適用範囲は？
- 生成物の権利関係：帰属・共有範囲・派生物の取り扱い
- モデルカード/データカードによる透明性の確保
- 倫理的配慮（バイアス、帰属、コミュニティの期待値）

---

<!-- p8: ディスカッションタイム -->
<!-- class: lead -->

# Discussion Time — 20分間！

取り上げるテーマ（再掲）

1. AIによるマッピング支援の現状と未来
2. ローカルLLM / Open Source AI の活用
3. ライセンスと倫理 (ODbL vs AI)

会場からの意見・事例・質問を歓迎します。
HackMDにメモを残しながら進めます。

---

<!-- p9: まとめ (Wrap-up) -->

## Wrap-up / 次のアクション

- 今日の論点をHackMDで整理して公開します
- 継続議論の場（Discord コミュニティ）につなげます

ご参加ありがとうございました。引き続き、OSM × Open Source AI の 健全で創造的な発展に向けて、ご協力をお願いします。
