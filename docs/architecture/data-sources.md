# データソース

Knowledge Catalog は、Google Cloud のサービスからメタデータを自動で取り込みます。
たとえば BigQuery にテーブルを作ると、操作をしなくてもそのテーブルがカタログに登録されます。

## 自動で取り込まれる Google Cloud のソース

| ソース | 取り込まれるもの |
|---|---|
| BigQuery | データセット、テーブル、ビュー、モデル、ルーティン、接続、リンクされたデータセット、グラフ（Preview） |
| BigQuery sharing | エクスチェンジ、リスティング |
| Cloud Storage | 自動検出されたデータ |
| Vertex AI | モデル、データセット、feature group など |
| Looker | ダッシュボード、Look、LookML、Explore、ビューなど |
| データベース | Bigtable、Spanner、AlloyDB for PostgreSQL（Preview）、Cloud SQL |
| その他 | Dataform、Dataproc Metastore、Iceberg REST Catalog、Pub/Sub、Datastream |

AlloyDB と Cloud SQL は、連携を有効化してから取り込まれます。
対象はプライマリインスタンスだけです。

## 自動で取り込まれないソース

Google Cloud の外にあるデータソースは、コネクタや自前のインポートで取り込みます。
方法は [分離された外部データソースからのメタデータ取り込み](../questions/isolated-external-sources.md) にあります。

## 関連

- [全体像](../overview.md) の層①
- 公式ドキュメント（2026-11-13 確認）: [メタデータモデル](https://docs.cloud.google.com/knowledge-catalog/docs/metadata-overview)
