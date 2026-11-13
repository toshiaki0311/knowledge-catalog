# Context Graph

[全体像](../全体像.md) › ② Knowledge Catalog 層

技術スキーマ、業務上の意味、データ間の関係、運用上の挙動、信頼シグナルを組み合わせたナレッジグラフ。\
[メタデータモデル](メタデータモデル.md) の Entry がノード、Entry Link がエッジになり、[Knowledge Studio](Knowledge-Studio.md) では対話的に操作できる図として表示される。

たとえば `customer_orders` テーブルのノードから、結合できる `customers` テーブルと、`email_address` 列の意味を定義する用語をたどることができる。

## ノード

- テーブル、ビュー
- データベース、ストレージ、AI のリソース
- Looker、dbt、Databricks Unity Catalog などサードパーティの資産
- ビジネス用語集の用語
- データプロダクト
- [Context Sets](Context-Sets.md)、ナレッジベースの文書
- カスタム資産

## エッジ

Knowledge Studio の表示では、Schema join、Definition、Reference、Context、Packages に分かれる。\
Schema join は BigQuery のジョブ解析から得た結合関係。

## データリネージとの違い

| | Context Graph | データリネージ |
|---|---|---|
| 表すもの | 業務上の意味と関係 | データの移動と変換 |
| 形 | 複数種類のノードを持つ意味のネットワーク | 有向非巡回グラフ |

## 関連

- 公式ドキュメント（2026-11-13 確認）: [データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)、[Knowledge Studio](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio)
