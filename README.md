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

### 用語集（glossary）

| 用語 | 意味 |
|---|---|
| [Schema join](docs/glossary/Schema-join.md) | テーブルどうしを結ぶ Context Graph のエッジ |
| [Definition](docs/glossary/Definition.md) | 技術的なデータ資産や列を、対応するビジネス用語集の定義に結ぶ Context Graph のエッジ |
| [Reference](docs/glossary/Reference.md) | Context Set の文書やデータ資産の Entry を、それが説明するカタログ上の資産に結ぶ、向きのある Context Graph のエッジ |
| [Context](docs/glossary/Context.md) | Context Set やドメインの文書を、対象のデータ資産に帰属させる Context Graph のエッジ |
| [Packages](docs/glossary/Packages.md) | どのデータ資産がどの データプロダクト にまとめられているかを示す、集約の Context Graph のエッジ |
| [信頼シグナル](docs/glossary/信頼シグナル.md) | 資産が正式な情報源として信頼できるかを確かめるための指標 |
| [グラウンディング](docs/glossary/グラウンディング.md) | AI エージェントの回答を、カタログにある業務のコンテキストに基づかせること |
| [データプロダクト](docs/glossary/データプロダクト.md) | 見つけやすく、信頼でき、利用できるように正式にパッケージ化された、データ資産の論理的なまとまり |
| [Change request](docs/glossary/Change-request.md) | エンリッチメントエージェントが提案した変更を、承認されるまで保留しておく単位 |
| [Overlay の Entry](docs/glossary/Overlay-entry.md) | エンリッチメントで生成された説明、概念、列と用語集の対応を、Context Set の中に保存する Entry |
| [クエリテンプレート](docs/glossary/クエリテンプレート.md) | 検証済みでパラメータ化された SQL を、自然言語の質問に結びつけて保存するもの |
| [MCP](docs/glossary/MCP.md) | Knowledge Catalog が提供する MCP サーバーの種類、ツール、認証 |
| [LookupContext API](docs/glossary/LookupContext-API.md) | 1 回のリクエストで、LLM 向けに整形済みのメタデータのまとまりを取得する API |
| [Iceberg REST Catalog](docs/glossary/Iceberg-REST-Catalog.md) | Apache Iceberg のテーブルと名前空間のメタデータを、REST のエンドポイントで公開するカタログ |
| [Lakehouse runtime catalog](docs/glossary/Lakehouse-runtime-catalog.md) | リモートの Iceberg REST Catalog のエンドポイントに接続し、テーブルのメタデータを同期する Google Cloud Lakehouse のカタログ |
| [Network attachment](docs/glossary/Network-attachment.md) | プライベート IP しか持たない外部のデータベースへ、BigQuery Data Transfer Service が Private Service Connect で接続するために用意するもの |

## 管理方針

資料を追加する手順と原則は [CLAUDE.md](CLAUDE.md) にある。
