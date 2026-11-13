# 付加情報・管理機能

メタデータに業務上の意味と信頼シグナルを足す機能です。

## 機能

| 機能 | 内容 | 公式ドキュメント |
|---|---|---|
| Business glossary | 用語集、カテゴリ、用語で業務用語の分類体系を作る。用語は `definition` や `synonym` の Entry Link で Entry や列に対応づける | [用語集の管理](https://docs.cloud.google.com/knowledge-catalog/docs/manage-glossaries) |
| Data lineage | パイプラインをまたいで、列レベルの変換を追跡する | [リネージ](https://docs.cloud.google.com/knowledge-catalog/docs/use-lineage) |
| Data profiling | スキャンで distinct count、null の割合、サンプル値などの統計分布を計算し、スキーマの異常や統計的なドリフトを検出する | [データプロファイリング](https://docs.cloud.google.com/knowledge-catalog/docs/data-profiling-overview) |
| Auto data quality | ルールベースの品質チェックを実行し、スコアを Entry に付ける | [自動データ品質](https://docs.cloud.google.com/knowledge-catalog/docs/auto-data-quality-overview) |
| Data insights | Gemini in BigQuery がクエリ履歴などから、列の説明、テーブル間の関係、クエリ例を生成する | [データインサイト](https://docs.cloud.google.com/knowledge-catalog/docs/data-insights-structured-data) |

## 関連

- [全体像](../overview.md) の層②
- Entry Link の種類: [メタデータモデル](metadata-model.md)
- AI による拡充の進め方: [エンリッチメントタスク](enrichment-tasks.md)
- 公式ドキュメント（2026-11-13 確認）: [Knowledge Catalog の概要](https://docs.cloud.google.com/knowledge-catalog/docs/introduction)
