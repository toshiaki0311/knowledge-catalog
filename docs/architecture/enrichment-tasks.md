# エンリッチメントタスク

エンリッチメントエージェントが対象のデータ資産を分析し、メタデータの追加や変更を提案する仕組みです。
[Knowledge Studio](knowledge-studio.md) の Enrichments から使います。

## 用語

| 用語 | 意味 |
|---|---|
| enrichment task | エージェントが対象の資産をどう分析するかを定めた設定 |
| enrichment job | バックエンドで動く実行処理 |
| enrichment run | 1 回の実行 |

## 生成されるもの

- テーブルの概要と列の定義
- 業務概念。用語の定義と KPI の計算式
- 列と用語集の定義の対応
- 検証済みの結合条件と、主キー・外部キーなどの関係
- パラメータ付きの SQL クエリテンプレート

## 実行の流れ

1. オンデマンドまたはスケジュールで実行を始める。
2. シグナルと文書を分析する。
3. 提案を下書きする。
4. SQL の構文を検証し、信頼度のスコアを付ける。評価セットがあれば精度を比べる。
5. 変更を change request として保留する。
6. キュレーターが差分を確認して承認する。

承認された内容は、[Context Sets](context-sets.md) の中に overlay の Entry として保存されます。
BigQuery のリソースに付いている説明は上書きされません。

## 自動公開の条件

次をすべて満たす提案は自動で承認され、監査記録が残ります。

- 全体の信頼度が 0.85 以上
- 妥当性のエラーがない
- 評価セットがある場合、精度の低下が 5 ポイント以内

削除の提案は必ず人がレビューします。

## 関連

- [全体像](../overview.md) の層③
- Knowledge Catalog 本体の拡充機能: [付加情報・管理機能](enrichment-features.md)
- 公式ドキュメント（2026-11-13 確認）: [エンリッチメントタスクについて](https://docs.cloud.google.com/knowledge-catalog/docs/about-enrichment-tasks)、[エンリッチメントの実行管理](https://docs.cloud.google.com/knowledge-catalog/docs/manage-enrichment-runs)
