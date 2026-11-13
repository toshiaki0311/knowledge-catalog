# Schema join

[全体像](../全体像.md) › 用語集

テーブルどうしを結ぶ Context Graph のエッジ。\
検証済みの複数テーブルの結合経路、主キー、外部キーを表す。

## 作られ方

BigQuery のジョブが自動でスキャンされ、異なるテーブルの列が同じ意味を持つことを示すクエリから作られる。

## 例

`customer_orders` と `customers` が顧客 ID で結合できるという関係。説明用の例。

## Entry Link Type との対応

[メタデータモデル](../architecture/メタデータモデル.md) の Entry Link Type に同名の `schema-join` がある。\
エッジとの対応は公式ドキュメントに明記されていない。

## 関連

- 使われている資料: [Context Graph](../architecture/Context-Graph.md)
- 公式ドキュメント（2026-11-13 確認）: [Knowledge Studio](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio)、[データ資産の探索](https://docs.cloud.google.com/knowledge-catalog/docs/explore-data-assets)
