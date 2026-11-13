# メタデータモデル

データ資産を Entry として表し、Aspect でメタデータを付け、Entry Link で資産どうしの関係を表します。

## コンポーネント

| コンポーネント | 役割 | 具体例 |
|---|---|---|
| Entry Group | Entry をまとめる管理単位 | 販売データ群 |
| Entry | データ資産を表現 | 売上テーブル |
| Entry Type | Entry の種類・構造を定義 | BigQuery Table |
| Aspect Type | メタデータの項目構造を定義 | 管理責任者、更新頻度 |
| Aspect | 実際のメタデータ | 管理責任者＝営業部 |
| Entry Link | データや概念の関係を表す | 売上→店舗 |

## 関連

- [全体像](../overview.md) の層②
- データに意味を付与する仕組み: [付加情報・管理機能](enrichment-features.md)、[Context Graph](context-graph.md)
- 公式ドキュメント: [メタデータモデル](https://docs.cloud.google.com/knowledge-catalog/docs/metadata-overview?hl=ja)
