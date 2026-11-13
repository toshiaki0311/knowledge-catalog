# Knowledge Catalog の全体像

Knowledge Catalog は、構造化・非構造化データにまたがって技術メタデータと業務上の意味を統合する Google Cloud のサービスです。
旧称は Dataplex Universal Catalog です。
データ資産の発見、データ品質の検証、生成 AI アプリのグラウンディングに使います。

メタデータは集約、拡充、検索と取得の 3 段階で扱われます。
段階の内容は [メタデータのライフサイクル](architecture/metadata-lifecycle.md) にあります。

## 4 つの層

この資料群での整理であり、公式の区分ではありません。

| 層 | 構成要素 | 資料 |
|---|---|---|
| ① データソース層 | BigQuery、Cloud Storage、外部 DB など | [データソース](architecture/data-sources.md) |
| ② Knowledge Catalog 層 | メタデータ管理 | [メタデータモデル](architecture/metadata-model.md)、[コンポーネント間の関係](architecture/component-relationships.md) |
| ② Knowledge Catalog 層 | 付加情報・管理機能 | [付加情報・管理機能](architecture/enrichment-features.md) |
| ② Knowledge Catalog 層 | Context Graph | [Context Graph](architecture/context-graph.md) |
| ③ コンテキスト整備・提供層 | Knowledge Studio | [Knowledge Studio](architecture/knowledge-studio.md)、[エンリッチメントタスク](architecture/enrichment-tasks.md) |
| ③ コンテキスト整備・提供層 | Context Sets | [Context Sets](architecture/context-sets.md) |
| ③ コンテキスト整備・提供層 | MCP、API | [コンテキストの取得手段](architecture/context-retrieval.md) |
| ④ 利用層 | AI エージェント、Conversational Analytics など | [利用側](architecture/consumers.md) |

## 全体構成図

![Knowledge Catalog の全体構成図](images/overview.png)

## 関連

- 公式ドキュメント（2026-11-13 確認）: [Knowledge Catalog の概要](https://docs.cloud.google.com/knowledge-catalog/docs/introduction)、[データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)
