# Lakehouse runtime catalog

[全体像](../全体像.md) › 用語集

リモートの [Iceberg REST Catalog](Iceberg-REST-Catalog.md) のエンドポイントに接続し、テーブルのメタデータを同期する Google Cloud Lakehouse のカタログ。

## 役割

OIDC か Secret Manager で認証する。\
Knowledge Catalog は、Lakehouse からメタデータとリネージを同期する。

## 補足

正式な定義のあるページは確認していない。

## 関連

- 使われている資料: [分離された外部データソースからのメタデータ取り込み](../questions/分離された外部データソースからのメタデータ取り込み.md)
- 公式ドキュメント（2026-11-13 確認）: [クロスクラウドのデータアクセス](https://docs.cloud.google.com/lakehouse/docs/about-cross-cloud-data-access)
