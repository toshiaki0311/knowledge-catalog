# knowledge-catalog

Google Cloud の Knowledge Catalog の知識を、全体像から個別トピックへ広げながら蓄積するリポジトリです。

## 目次

| 資料 | 内容 |
|---|---|
| [全体像](docs/overview.md) | 4 つの層と全体構成図 |
| [調査予定](docs/backlog.md) | これから資料にするトピック |

### 構成（architecture）

| 資料 | 内容 |
|---|---|
| [データソース](docs/architecture/data-sources.md) | メタデータの収集元 |
| [メタデータモデル](docs/architecture/metadata-model.md) | Entry、Aspect、Entry Link によるデータ資産の表現 |
| [付加情報・管理機能](docs/architecture/enrichment-features.md) | 用語、来歴、プロファイル、品質、AI による説明 |
| [Context Graph](docs/architecture/context-graph.md) | 資産・用語・関係性を統合する論理グラフ |
| [コンテキストの整備と提供](docs/architecture/context-delivery.md) | Knowledge Studio、Context Sets、MCP と API |
| [利用側](docs/architecture/consumers.md) | コンテキストを使う AI エージェントと分析ツール |

## 管理方針

資料を追加する手順と原則は [CLAUDE.md](CLAUDE.md) にあります。
