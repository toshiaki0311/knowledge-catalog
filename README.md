# knowledge-catalog

Google Cloud の Knowledge Catalog の知識を、全体像から個別トピックへ広げながら蓄積するリポジトリです。

## 目次

| 資料 | 内容 |
|---|---|
| [全体像](docs/overview.md) | サービスの定義、全体構成図、層ごとの資料 |
| [調査予定](docs/backlog.md) | これから資料にするトピック |

### 構成（architecture）

| 資料 | 内容 |
|---|---|
| [メタデータのライフサイクル](docs/architecture/metadata-lifecycle.md) | 集約、拡充、検索と取得の 3 つの柱 |
| [データソース](docs/architecture/data-sources.md) | メタデータの収集元と取り込み方法 |
| [メタデータモデル](docs/architecture/metadata-model.md) | Entry、Aspect、Entry Link とその型、包含と参照の関係 |
| [付加情報・管理機能](docs/architecture/enrichment-features.md) | 用語集、リネージ、プロファイリング、品質、インサイト |
| [Context Graph](docs/architecture/context-graph.md) | 資産、業務上の意味、関係を統合するナレッジグラフ |
| [Knowledge Studio](docs/architecture/knowledge-studio.md) | コンテキストを整備する画面 |
| [Context Sets](docs/architecture/context-sets.md) | AI エージェントに渡す知識のまとまり |
| [エンリッチメントタスク](docs/architecture/enrichment-tasks.md) | AI によるメタデータの提案と承認 |
| [コンテキストの取得手段](docs/architecture/context-retrieval.md) | MCP サーバーと API |
| [利用側](docs/architecture/consumers.md) | コンテキストを使う AI エージェントと分析ツール |

## 管理方針

資料を追加する手順と原則は [CLAUDE.md](CLAUDE.md) にあります。
