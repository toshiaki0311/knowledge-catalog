# メタデータモデル

Knowledge Catalog は、データ資産を Entry として表し、Aspect でメタデータを付け、Entry Link で資産どうしの関係を表します。
要素どうしの包含と参照は [コンポーネント間の関係](component-relationships.md) にあります。

## 構成要素

| 要素 | 定義 | 具体例 |
|---|---|---|
| Entry Group | Entry と Entry Link を入れるリージョン単位のコンテナ。管理とセキュリティの境界になる | `@bigquery` |
| Entry | 単一のデータ資産を表す | BigQuery のテーブル |
| Entry Type | Entry の構造と必須の Aspect を定めるテンプレート | BigQuery テーブル用の型 |
| Aspect Type | Aspect のフィールド、データ型、検証ルールを定める再利用可能なスキーマ | `Schema`、`DataQuality` |
| Aspect | Aspect Type に従う、関連するメタデータフィールドの集まり | 列の定義、所有者 |
| Entry Link | 2 つの Entry、または Entry 内の列どうしの意味的な関係 | 用語と列の対応 |
| Entry Link Type | Entry Link の種類 | `definition` |

## Aspect の付与先

Aspect は Entry、Entry の列、Entry Link の 3 か所に付きます。
列は `schema` の Aspect を Entry に付けると生成され、ネストは `customer.address.postal_code` のようにドットで表します。
`schema-join` の Entry Link には Aspect を付けられません。

## Entry Link Type

| 種類 | 用途 | 方向 |
|---|---|---|
| `definition` | ビジネス用語集の定義を、物理的な列や Entry に結ぶ | あり |
| `synonym` | 同等の業務概念や別名の用語を結ぶ | なし |
| `related` | システムをまたぐ、ゆるく関連する資産を結ぶ | なし |
| `schema-join` | 外部キーなどで結合できるテーブルを結ぶ | なし |

## システム提供とユーザー定義

| 要素 | システム提供 | ユーザー定義 |
|---|---|---|
| Entry Group | Google Cloud サービス用にプロジェクトごとに作られる。`@bigquery`、`@spanner`、`@pubsub` など | カスタム資産と権限管理のために作る |
| Entry | Google Cloud のソースから自動で作られる | 独自のデータソース、ファイル、外部 DB のために作る |
| Entry Type | Google Cloud のリソース種別を表す型 | カスタム資産向けに必須・任意の Aspect を定める |
| Aspect Type | `Schema`、`Overview`、`Contacts`、`DataQuality`、`Lineage` など | PII 分類や SLA の階層など |
| Aspect | ソースシステム、クエリログ、自動スキャンから作られる | 利用者、パイプライン、エージェントが付ける |

## 関連

- [全体像](../overview.md) の層②
- 公式ドキュメント（2026-11-13 確認）: [メタデータモデル](https://docs.cloud.google.com/knowledge-catalog/docs/metadata-overview)
