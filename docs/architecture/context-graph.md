# Context Graph

技術スキーマ、業務上の意味、データ間の関係、運用上の挙動、信頼シグナルを組み合わせたナレッジグラフです。
[メタデータモデル](metadata-model.md) の Entry がノード、Entry Link がエッジになり、[Knowledge Studio](knowledge-studio.md) では対話的に操作できる図として表示されます。

たとえば `customer_orders` テーブルのノードから、結合できる `customers` テーブルと、`email_address` 列の意味を定義する用語をたどれます。

## ノード

- テーブル、ビュー
- データベース、ストレージ、AI のリソース
- Looker、dbt、Databricks Unity Catalog などサードパーティの資産
- ビジネス用語集の用語
- データプロダクト
- [Context Sets](context-sets.md)、ナレッジベースの文書
- カスタム資産

## エッジ

Knowledge Studio の表示では、Schema join、Definition、Reference、Context、Packages に分かれます。
Schema join は BigQuery のジョブ解析から得た結合関係です。

## データリネージとの違い

| | Context Graph | データリネージ |
|---|---|---|
| 表すもの | 業務上の意味と関係 | データの移動と変換 |
| 形 | 複数種類のノードを持つ意味のネットワーク | 有向非巡回グラフ |

## 関連

- [全体像](../overview.md) の層②
- 公式ドキュメント（2026-11-13 確認）: [データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)、[Knowledge Studio](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio)
