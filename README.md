# knowledge-catalog

Google Cloud の Knowledge Catalog の知識を、全体像から個別トピックへ広げながら蓄積するリポジトリ。

## 目次

| 資料 | 内容 |
|---|---|
| [全体像](docs/全体像.md) | サービスの定義、全体構成図、一連の流れ。最初に読む資料 |
| [調査予定](docs/調査予定.md) | 知りたいトピックと、裏が取れていない点 |

### 構成（architecture）

| 資料 | 内容 |
|---|---|
| [メタデータのライフサイクル](docs/architecture/メタデータのライフサイクル.md) | 集約、拡充、検索と取得の 3 つの柱 |
| [データソース](docs/architecture/データソース.md) | メタデータの収集元と取り込み方法 |
| [メタデータモデル](docs/architecture/メタデータモデル.md) | Entry、Aspect、Entry Link とその型、包含と参照の関係 |
| [付加情報・管理機能](docs/architecture/付加情報・管理機能.md) | 用語集、リネージ、プロファイリング、品質、インサイト |
| [Context Graph](docs/architecture/Context-Graph.md) | 資産、業務上の意味、関係を統合するナレッジグラフ |
| [Knowledge Studio](docs/architecture/Knowledge-Studio.md) | コンテキストを整備する画面 |
| [Context Sets](docs/architecture/Context-Sets.md) | AI エージェントに渡す知識のまとまり |
| [エンリッチメントタスク](docs/architecture/エンリッチメントタスク.md) | AI によるメタデータの提案と承認 |
| [コンテキストの取得手段](docs/architecture/コンテキストの取得手段.md) | MCP サーバーと API |
| [利用側](docs/architecture/利用側.md) | コンテキストを使う AI エージェントと分析ツール |

### 気になること（questions）

| 資料 | 内容 |
|---|---|
| [分離された外部データソースという状況は起こるか](docs/questions/分離された外部データソースという状況は起こるか.md) | エージェントからは届くが Knowledge Catalog とは分離されたデータソースが生じる場面 |
| [分離された外部データソースからのメタデータ取り込み](docs/questions/分離された外部データソースからのメタデータ取り込み.md) | 別クラウド、SaaS、オンプレミスにあるデータソースの取り込み方法 |

## 管理方針

資料を追加する手順と原則は [CLAUDE.md](CLAUDE.md) にある。
