# メタデータのライフサイクル

Knowledge Catalog はメタデータを 3 つの柱で扱います。

| 柱 | 公式の呼び方 | 内容 | 例 |
|---|---|---|---|
| 集約 | Aggregation（Discover and ingest） | 物理データを動かさずに、技術メタデータを自動でクロールしてインデックス化する | BigQuery のテーブルが、列の一覧とともにカタログに登録される |
| 拡充 | Enrichment（Curate context and verify trust） | 業務上の意味を付与し、信頼シグナルを確立する | 列に用語の定義を結びつけ、品質チェックの結果を付ける |
| 検索と取得 | Search and retrieval（Access and ground） | AI アプリやユーザーが Context Graph に問い合わせる | エージェントが、質問に関係するテーブルと用語の定義を取得する |

## 関連

- [全体像](../overview.md)
- 公式ドキュメント（2026-11-13 確認）: [Knowledge Catalog の概要](https://docs.cloud.google.com/knowledge-catalog/docs/introduction)
