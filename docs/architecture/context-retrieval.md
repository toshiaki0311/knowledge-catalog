# コンテキストの取得手段

AI エージェントやアプリは、MCP サーバーか API で Knowledge Catalog のコンテキストを取得します。

## 手段

| 手段 | 内容 |
|---|---|
| リモート MCP サーバー | Google がホストする HTTP エンドポイント。`https://dataplex.googleapis.com/mcp` |
| ローカル MCP サーバー | MCP Toolbox を使い、IDE などから標準入出力で接続する |
| LookupContext API | REST と gRPC。コンテキストを YAML か JSON で返す。`BASIC` と `STANDARD` のビューがあり、`context_budget` でトークンの予算を指定できる |
| ListEntries、LookupEntry | Entry を取得する Knowledge Catalog API。[Context Sets](context-sets.md) の中身の取得に使える |
| セマンティック検索 | 自然言語で資産を探す。アクセス権と業務用語を踏まえて結果を返す |

Entry や Aspect Type の作成・更新には、CreateEntry などの Knowledge Catalog API を使います。

## 取得の 2 つのパターン

| パターン | 内容 |
|---|---|
| 動的な発見 | ユーザーの質問ごとに、セマンティック検索で関連する Context Set を探す |
| 事前に指定 | エージェントの設定に Context Set のリソース名を指定し、ルートインデックスから読む |

## 関連

- [全体像](../overview.md) の層③
- 取得する側: [利用側](consumers.md)
- 公式ドキュメント（2026-11-13 確認）: [MCP の概要](https://docs.cloud.google.com/knowledge-catalog/docs/mcp-overview)、[データコンテキストの取得](https://docs.cloud.google.com/knowledge-catalog/docs/retrieve-data-context)、[資産の検索](https://docs.cloud.google.com/knowledge-catalog/docs/search-assets)
