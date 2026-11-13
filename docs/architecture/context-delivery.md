# コンテキストの整備と提供

Knowledge Studio で拡充とレビューを行い、Context Sets で渡す範囲を決め、MCP や API で取得させます。
Knowledge Studio と Context Sets は Knowledge Catalog と一体的に機能し、独立したデータ保存基盤ではありません。

## コンポーネント

| コンポーネント | 主な役割 |
|---|---|
| Knowledge Studio | コンテキストの探索・拡充・レビュー |
| Context Sets | AI に渡す知識の範囲を整理 |
| MCP / Context API / Catalog APIs | AI がコンテキストを取得するための接続手段 |

## 関連

- [全体像](../overview.md) の層③
- 公式ドキュメント: [Knowledge Studio のアーキテクチャ](https://docs.cloud.google.com/knowledge-catalog/docs/knowledge-studio?hl=ja)
