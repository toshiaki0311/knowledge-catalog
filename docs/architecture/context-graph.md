# Context Graph

技術スキーマ、業務上の意味、データ間の関係、運用上の挙動、信頼シグナルを組み合わせたナレッジグラフです。
Knowledge Catalog の Entry と Entry Link で構成され、[Knowledge Studio](knowledge-studio.md) では対話的に操作できる図として表示されます。

## コンテキストの 6 つの層

技術メタデータ、セマンティックメタデータ、運用メタデータ、関係性、信頼シグナル、エージェント向けガイダンス。

## ノード

- テーブル、ビュー
- データベース、ストレージ、AI のリソース
- Looker、dbt、Databricks Unity Catalog などサードパーティの資産
- ビジネス用語集の用語
- データプロダクト
- [Context Sets](context-sets.md)、ナレッジベースの文書
- カスタム資産

## エッジ

| 種類 | 表す関係 |
|---|---|
| Schema join | BigQuery のジョブ解析から得た結合関係 |
| Definition | 列と用語集の定義の対応 |
| Reference | 他の Entry への参照 |

ほかに Context と Packages があります。

## データリネージとの違い

| | Context Graph | データリネージ |
|---|---|---|
| 表すもの | 業務上の意味と関係 | データの移動と変換 |
| 形 | 複数種類のノードを持つ意味のネットワーク | 有向非巡回グラフ |

## 関連

- [全体像](../overview.md) の層②
- グラフを構成する要素: [メタデータモデル](metadata-model.md)
- 公式ドキュメント（2026-11-13 確認）: [データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)、[Knowledge Studio](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio)
