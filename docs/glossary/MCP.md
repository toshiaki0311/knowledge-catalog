# MCP

[全体像](../全体像.md) › 用語集

Knowledge Catalog は、AI エージェントがカタログのメタデータを検索・取得するための MCP サーバーを提供する。\
Dataplex API を有効にすると、リモートの MCP サーバーも自動で有効になる。

## サーバーの種類

| 種類 | 接続先 | 用途 |
|---|---|---|
| リモート | `https://dataplex.googleapis.com/mcp` | メタデータの検索とコンテキストの取得 |
| リモート | `https://dataplex.googleapis.com/mcp/data-products` | [データプロダクト](データプロダクト.md) とデータ資産の作成、取得、更新 |
| ローカル | 手元で動かす MCP Toolbox。`--prebuilt dataplex` を指定する | IDE やコーディングエージェントからの検索と取得 |
| データリネージ用のリモート | `https://datalineage.googleapis.com/mcp` | リネージの検索。Preview |

## ツール

| ツール | 内容 | サーバー |
|---|---|---|
| `search_entries` | 検索構文でデータ資産を探す | リモート、ローカル |
| `lookup_entry` | 1 つの Entry のスキーマや Aspect を、そのままの構造で取得する | リモート、ローカル |
| `lookup_context` | 指定した資産について、LLM 向けに整形したコンテキストを YAML で取得する。1 回に最大 10 件 | リモート、ローカル |
| `search_aspect_types` | ガバナンスのルールや分類を探す | ローカル |
| `create_data_product` など | データプロダクトとデータ資産を作成、更新する | データプロダクト用のリモート |
| `search_lineage` | 資産の上流または下流のリネージをたどる。列レベルにも対応する | データリネージ用のリモート |

`search_entries`、`lookup_entry`、`lookup_context` は読み取り専用。\
要約されたコンテキストが欲しいときは `lookup_context`、生のメタデータが欲しいときは `lookup_entry` を使う。

## 例

エージェントが `system:bigquery AND type:table AND name:customers` で `search_entries` を呼び、見つかったテーブルを `lookup_context` に渡して、スキーマ、データ品質、関連する資産を受け取る。

## 関連

- 公式ドキュメント: [MCP の概要](https://docs.cloud.google.com/knowledge-catalog/docs/mcp-overview)、[リモート MCP サーバーの利用](https://docs.cloud.google.com/knowledge-catalog/docs/use-remote-mcp)、[MCP Toolbox の利用](https://docs.cloud.google.com/knowledge-catalog/docs/pre-built-tools-with-mcp-toolbox)、[データリネージの MCP サーバー](https://docs.cloud.google.com/knowledge-catalog/docs/use-lineage-mcp)、[MCP リファレンス](https://docs.cloud.google.com/knowledge-catalog/docs/reference/mcp)
