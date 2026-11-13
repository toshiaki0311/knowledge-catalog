# LookupContext API

[全体像](../全体像.md) › 用語集

1 回のリクエストで、LLM 向けに整形済みのメタデータのまとまりを取得する API。

## 入力

コンテキストを取得する Entry の名前を最大 10 個。出力の形式。`context_budget` で応答の文字数の上限。

## 出力

整形済みのテキスト。技術メタデータ、運用メタデータ、業務上の説明、データプロファイル、データ品質、関連する資産を含む。\
呼び出した ID が IAM の権限を持つ資産だけが返る。

## 関連

- 使われている資料: [コンテキストの取得手段](../architecture/コンテキストの取得手段.md)
- 公式ドキュメント（2026-11-13 確認）: [データコンテキストの取得](https://docs.cloud.google.com/knowledge-catalog/docs/retrieve-data-context)
