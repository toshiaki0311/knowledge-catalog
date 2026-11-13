# Context Graph

[全体像](../全体像.md) › ② Knowledge Catalog 層

技術スキーマ、業務上の意味、データ間の関係、運用上の挙動、[信頼シグナル](../glossary/信頼シグナル.md)を組み合わせたナレッジグラフ。\
[メタデータモデル](メタデータモデル.md) の Entry がノード、Entry Link がエッジになり、[Knowledge Studio](Knowledge-Studio.md) では対話的に操作できる図として表示される。

たとえば `customer_orders` テーブルのノードから、結合できる `customers` テーブルと、`email_address` 列の意味を定義する用語をたどることができる。

## ノード

- テーブル、ビュー
- データベース、ストレージ、AI のリソース
- Looker、dbt、Databricks Unity Catalog などサードパーティの資産
- ビジネス用語集の用語
- [データプロダクト](../glossary/データプロダクト.md)
- [Context Sets](Context-Sets.md)、ナレッジベースの文書
- カスタム資産

## エッジ

Knowledge Studio の表示では、次の種類に分かれる。

| 種類 | 結ぶもの |
|---|---|
| [Schema join](../glossary/Schema-join.md) | テーブルとテーブル |
| [Definition](../glossary/Definition.md) | 列やデータ資産と、用語集の定義 |
| [Reference](../glossary/Reference.md) | Context Set の文書やデータ資産の Entry と、それが説明する資産 |
| [Context](../glossary/Context.md) | Context Set や文書と、対象のデータ資産 |
| [Packages](../glossary/Packages.md) | データ資産と、データプロダクト |

## データリネージとの違い

| | Context Graph | データリネージ |
|---|---|---|
| 表すもの | 業務上の意味と関係 | データの移動と変換 |
| 形 | 複数種類のノードを持つ意味のネットワーク | 有向非巡回グラフ |

## 関連

- 公式ドキュメント（2026-11-13 確認）: [データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)、[Knowledge Studio](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio)
