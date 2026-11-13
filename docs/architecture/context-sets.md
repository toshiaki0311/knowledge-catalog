# Context Sets

[全体像](../overview.md) › ③ コンテキスト整備・提供層

意味の情報とデータ資産への参照を、範囲を区切ってまとめたコンテナです。\
AI エージェントに渡す知識をドメインごとに束ね、際限のない検索をさせないための境界になります。

たとえば販売分析用の Context Set には、注文テーブルの説明、用語「売上」の定義、月次売上を出すクエリテンプレートを入れます。

## 実体

Context Set は `type="context-set"` の特殊な [Entry Group](metadata-model.md) です。\
中身はカスタムの Entry と Aspect として Knowledge Catalog に保存され、業務用語、SQL テンプレート、Markdown の文書は Aspect に入ります。

## 中身

| Entry の種類 | 内容 | パス |
|---|---|---|
| ルートインデックス | エージェントが最初に読む入口 | `agents` |
| ディレクトリインデックス | 配下の一覧 | `assets`、`documents` |
| データ資産 | テーブルごとのコンテキスト | `assets/bigquery/PROJECT/DATASET/TABLE` |
| 業務概念 | 用語の定義、KPI の計算式 | `documents/concepts/*` |
| ナレッジベース | ガイドラインなどの文書 | `documents/*` |
| ラーニング | 学習内容の文書 | `documents/learnings/*` |
| クエリテンプレート | パラメータ付きの SQL。意図、自然言語の質問、クエリ、パラメータを持つ | |

## 他の要素との関係

| 相手 | 関係 |
|---|---|
| [Context Graph](context-graph.md) | Context Set は Context Graph の中の、まとまった部分グラフ |
| 実テーブルの Entry | データ資産の Entry が `reference` の Entry Link で `@bigquery` などの Entry を参照する |
| データへのアクセス権 | Context Set は付与しない |
| データプロダクト | データプロダクトはデータそのものを共有・統治し、Context Set は会話用の意味をまとめる。データプロダクトから参照できる |

## Preview の制約

- 1 つの Context Set に設定できるエンリッチメントタスクは 1 つ
- Context Set をまたいで Entry の一部だけを参照することはできない

## 関連

- 公式ドキュメント（2026-11-13 確認）: [Context sets](https://docs.cloud.google.com/knowledge-catalog/docs/context-sets)
