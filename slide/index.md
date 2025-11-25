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

### 25min (16:30-16:55):
- Intro（キックオフプレゼン）: 5分
- Discussion（ディスカッション）: 20分

### 記録について:
- 会場から記録係を募集します（複数名OK）
- オンラインノートHackMD を利用

<br/>
 配信、記録があるため、マイクを使用してください。

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
2つのテーマを提示します。まず概要を共有し、その後みなさんの
経験・課題・アイデアを起点に深掘りしていきます。

---

<!-- p5: テーマ1 -->

## テーマ1: AIによるマッピング支援の現状と未来

- 例: Rapid Editor, JOSM MapWithAI などの支援ツール
- 自動化はどこまで許容される？品質管理・レビューとの両立は？
- 画像認識・物体検出の活用と限界

---

<!-- p5a: Rapid Editor と JOSM MapWithAI Plugin の紹介 -->

##  参考: Rapid Editor と JOSM MapWithAI Plugin

- Rapid Editor (RapiD): 機械学習で推定された道路・建物などの候補を提示し、編集を支援
- JOSM MapWithAI Plugin: JOSMでRapiD等の推定結果を活用し、レビュー/取り込みを効率化
- どちらも「人間による確認・判断」を前提に、作業効率を高めることが目的

参考リンク:
- RapiD: https://mapwith.ai/rapid / Wiki: https://wiki.openstreetmap.org/wiki/RapiD
- JOSM Plugin (MapWithAI): https://wiki.openstreetmap.org/wiki/JOSM/Plugins/MapWithAI

---

<!-- p6: テーマ2 -->

## テーマ2: ローカルLLM / Open Source AI の活用

- OSMデータを使った特化型モデル（地物タグ理解・提案）
- 自然言語でのクエリ検索（Overpass/TagInfoを補助する対話）
- エッジ/ローカル推論（オフライン環境、プライバシー配慮）

---

<!-- p8: ディスカッションタイム -->
<!-- class: lead -->

# Discussion Time — 20分間！

取り上げるテーマ（再掲）

1. AIによるマッピング支援の現状と未来
2. ローカルLLM / Open Source AI の活用

会場からの意見・事例・質問を歓迎します。
HackMDにメモを残しながら進めます。

---

<!-- p9: まとめ (Wrap-up) -->

## Wrap-up / 次のアクション

- 今日の論点をHackMDで整理して公開します
- 継続議論の場（Discord コミュニティ）につなげます
  
ご参加ありがとうございました。引き続き、OSM × Open Source AI の 健全で創造的な発展に向けて、ご協力をお願いします。

---

<!-- p5b: MapAI / GeoAI 支援ツールの概要 -->

## テーマ1参考: AI 支援ツールの例

- Mapillary: ストリートレベル画像＋AI検出（標識・道路属性）でマッピング支援
- ML Enabler: 機械学習の推論結果（建物/道路ポリゴン等）をOSM編集や課題化に繋ぐワークフロー基盤
- 画像や推論結果は、そのまま投入ではなく「目視確認＋ローカル知見」で検証するのが前提

参考リンク:
- Mapillary: https://www.mapillary.com/ （Wiki: https://wiki.openstreetmap.org/wiki/Mapillary）
- ML Enabler: https://github.com/developmentseed/ml-enabler

---

<!-- p5c: 品質管理（QA）のAIツール事例 -->

## テーマ1参考: 品質管理のAIツール例

- Robosat.pink: 画像セグメンテーションにより建物・道路等の候補を抽出→OSMとの差分から欠落/過検出をQA
- Microsoft ML Building Footprints × MapRoulette: ML建物フットプリントとOSM比較で課題化→コミュニティがレビュー
- AIは「自動修正」ではなく、QA課題生成・優先度付け・レビュー支援として活用するのが安心

参考リンク:
- Robosat.pink: https://github.com/remap-xyz/robosat.pink
- Microsoft ML Building Footprints: https://github.com/microsoft/USBuildingFootprints
- MapRoulette: https://maproulette.org/ （Wiki: https://wiki.openstreetmap.org/wiki/MapRoulette）

---
