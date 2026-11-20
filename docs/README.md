# 設計書一覧

## 基本設計

|設計ID|設計書|概要|
|---|---|---|
|SYS-BD-001|[システム概要設計](basic-design/01-system-overview.md)|目的、スコープ、主要ユースケース、用語、制約|
|SYS-BD-002|[システムアーキテクチャ](basic-design/02-system-architecture.md)|モジュラモノリス、論理構成、技術境界|
|SYS-BD-003|[モジュール設計](basic-design/03-module-design.md)|Coreと業務モジュール、依存方向、拡張方法|
|SYS-BD-004|[データベース基本設計](basic-design/04-database-basic.md)|テナント、共通エンティティ、テーブル方針|
|SYS-BD-005|[認証・認可設計](basic-design/05-authentication.md)|認証主体、ロール、権限、認可境界|
|SYS-BD-006|[テナント管理設計](basic-design/06-tenant.md)|テナントライフサイクル、分離、契約制御|
|SYS-BD-007|[ワークフロー基本設計](basic-design/07-workflow.md)|定義、状態遷移、承認者、バージョン管理|
|SYS-BD-008|[API基本設計](basic-design/08-api-basic.md)|REST規約、共通レスポンス、エラー、セキュリティ|
|SYS-BD-009|[画面基本設計](basic-design/09-ui-basic.md)|画面構成、共通状態、権限、レスポンシブ方針|
|SYS-BD-010|[通知機能設計](basic-design/10-notification.md)|通知種別、配信、リマインド、再送、将来連携|
|SYS-BD-011|[ログ・監査設計](basic-design/11-log-audit.md)|操作ログ、監査ログ、相関ID、保持方針|
|SYS-BD-012|[クラウド・オンプレミス構成](basic-design/12-deployment.md)|環境構成、ストレージ、外部連携、切替性|

## 詳細設計・テンプレート

- [詳細設計テンプレート](templates/detailed-design-template.md)
- [詳細設計一覧ディレクトリ](detailed-design/)
- [DB設計ディレクトリ](database/)
- [API設計ディレクトリ](api/)
- [UI設計ディレクトリ](ui/)
- [テスト設計ディレクトリ](test/)
- [運用設計ディレクトリ](operations/)

## トレーサビリティ規約

基本設計（`SYS-BD-*`） → 詳細設計（`SYS-DD-*`） → テーブル（`T-*`）／API（`A-*`）／画面（`UI-*`） → ソースコード → テスト（`TC-*`）。

未決定事項は各設計書に残し、暫定方針は「暫定」と明記する。
