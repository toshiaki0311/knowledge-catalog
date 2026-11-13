# メタデータのライフサイクル

Knowledge Catalog はメタデータを 3 つの柱で扱います。

## 3 つの柱

| 柱 | 公式の呼び方 | 内容 | 資料 |
|---|---|---|---|
| 集約 | Aggregation（Discover and ingest） | 物理データを動かさずに、技術メタデータを自動でクロールしてインデックス化する | [データソース](data-sources.md)、[メタデータモデル](metadata-model.md) |
| 拡充 | Enrichment（Curate context and verify trust） | 業務上の意味を付与し、信頼シグナルを確立する | [付加情報・管理機能](enrichment-features.md)、[エンリッチメントタスク](enrichment-tasks.md) |
| 検索と取得 | Search and retrieval（Access and ground） | AI アプリやユーザーが Context Graph に問い合わせる | [コンテキストの取得手段](context-retrieval.md)、[利用側](consumers.md) |

## AI エージェントに届くまでの流れ

| 順 | フェーズ | 内容 |
|---|---|---|
| 1 | Ingestion and discovery | データソースからメタデータを取り込む |
| 2 | Context mapping | 技術的な Aspect、ビジネス用語集、検証済みクエリを結びつけて [Context Graph](context-graph.md) を組み立てる |
| 3 | Delivery interfaces | MCP や LookupContext API でコンテキストを取得させる |
| 4 | Agent grounding | ADK や LangChain が、取得したメタデータを LLM のプロンプトに注入する |

## 関連

- [全体像](../overview.md)
- 公式ドキュメント（2026-11-13 確認）: [Knowledge Catalog の概要](https://docs.cloud.google.com/knowledge-catalog/docs/introduction)、[データコンテキストについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-context)
