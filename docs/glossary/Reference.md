# Reference

[全体像](../全体像.md) › 用語集

Context Set の文書やデータ資産の Entry を、それが説明するカタログ上の資産に結ぶ、向きのある Context Graph のエッジ。

## 作られ方

エンリッチメントが生成した Entry には自動で付く。\
Entry Link Type は `dataplex-types.global.reference`。

## 例

Context Set の中にある `customer_orders` の説明が、`@bigquery` にある `customer_orders` の Entry を指す。説明用の例。

## 関連

- 公式ドキュメント: [データ資産の探索](https://docs.cloud.google.com/knowledge-catalog/docs/explore-data-assets)、[Context sets](https://docs.cloud.google.com/knowledge-catalog/docs/context-sets)
