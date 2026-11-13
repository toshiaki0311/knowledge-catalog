# Knowledge Catalog の全体像

Knowledge Catalog は、構造化・非構造化データにまたがって技術メタデータと業務上の意味を統合する Google Cloud のサービスです。
旧称は Dataplex Universal Catalog です。
データ資産の発見、データ品質の検証、生成 AI アプリのグラウンディングに使います。

## 全体構成図

![Knowledge Catalog の全体構成図](images/overview.png)

4 つの層はこの資料群での整理であり、公式の区分ではありません。

## 層ごとの資料

| 層 | 資料 |
|---|---|
| 全体 | [メタデータのライフサイクル](architecture/metadata-lifecycle.md) |
| ① データソース層 | [データソース](architecture/data-sources.md) |
| ② Knowledge Catalog 層 | [メタデータモデル](architecture/metadata-model.md)、[付加情報・管理機能](architecture/enrichment-features.md)、[Context Graph](architecture/context-graph.md) |
| ③ コンテキスト整備・提供層 | [Knowledge Studio](architecture/knowledge-studio.md)、[Context Sets](architecture/context-sets.md)、[エンリッチメントタスク](architecture/enrichment-tasks.md)、[コンテキストの取得手段](architecture/context-retrieval.md) |
| ④ 利用層 | [利用側](architecture/consumers.md) |

## 関連

- 公式ドキュメント（2026-11-13 確認）: [Knowledge Catalog の概要](https://docs.cloud.google.com/knowledge-catalog/docs/introduction)、[データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)
