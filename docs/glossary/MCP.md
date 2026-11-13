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

## 例

エージェントが `customers` という名前の BigQuery のテーブルを検索し、見つかったテーブルのスキーマ、データ品質、関連する資産を受け取る。

## 関連

- 公式ドキュメント: [MCP の概要](https://docs.cloud.google.com/knowledge-catalog/docs/mcp-overview)、[リモート MCP サーバーの利用](https://docs.cloud.google.com/knowledge-catalog/docs/use-remote-mcp)、[MCP Toolbox の利用](https://docs.cloud.google.com/knowledge-catalog/docs/pre-built-tools-with-mcp-toolbox)、[データリネージの MCP サーバー](https://docs.cloud.google.com/knowledge-catalog/docs/use-lineage-mcp)、[MCP リファレンス](https://docs.cloud.google.com/knowledge-catalog/docs/reference/mcp)
