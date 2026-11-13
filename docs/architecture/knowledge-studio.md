# Knowledge Studio

企業のメタデータをキュレーションして統合し、生成 AI アプリを業務のコンテキストにグラウンディングさせるための画面です。
Preview の機能です。

## 3 つの領域

| 領域 | できること |
|---|---|
| New chat | 自然言語でのデータ探索と、[Context Graph](context-graph.md) の対話的な表示 |
| Context sets | [Context Sets](context-sets.md) の作成と管理 |
| Enrichments | [エンリッチメントタスク](enrichment-tasks.md) の設定、評価ベンチマークの設定、AI が提案した変更のレビュー |

## 入力になる情報

- BigQuery のテーブルとビュー、Lakehouse、データベース
- Cloud Storage 上の文書
- Confluence、Jira、GitHub などの外部ナレッジ
- Cloud Logging などのクエリ履歴
- Gemini Enterprise のチャットログ、BigQuery の agent analytics

## Preview の制約

- 操作は Google Cloud コンソールが中心で、エンリッチメントタスクの管理に REST API と gcloud は使えない
- VPC Service Controls と CMEK に対応していない

## 関連

- [全体像](../overview.md) の層③
- 整備した結果の取得: [コンテキストの取得手段](context-retrieval.md)
- 公式ドキュメント（2026-11-13 確認）: [Knowledge Studio](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio)
