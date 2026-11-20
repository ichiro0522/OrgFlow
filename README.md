# OrgFlow

中小企業向けの社内業務管理プラットフォームです。社員・組織を共通基盤とし、報告管理、承認ワークフロー、申請、通知、ファイル、監査を一元管理します。

## システムの目的

業種を問わない汎用的な業務基盤を提供し、テナントごとの組織構造、承認フロー、契約モジュール、将来機能を拡張可能な形で管理します。

## 技術スタック（確定方針）

- Backend: PHP / Laravel
- Frontend: Vue.js
- Database: PostgreSQL
- API: REST API
- Architecture: モジュラモノリス
- Platform: クラウド・オンプレミス双方
- 主キー: UUIDを原則

具体バージョン、認証方式、クラウド製品等は設計書の未決定事項として管理します。

## ディレクトリ構成

```text
.github/                 Copilotルール、エージェント、指示
docs/                    プロジェクト・基本・詳細・横断設計
src/backend/             Laravelバックエンドの配置先
src/frontend/            Vue.jsフロントエンドの配置先
tests/backend/           バックエンドテスト
tests/frontend/          フロントエンドテスト
tests/integration/       結合テスト
infrastructure/docker/   Docker構成
infrastructure/cloud/    クラウド構成
infrastructure/on-premises/ オンプレミス構成
scripts/                 開発、DB、デプロイ補助
```

## 開発環境の構築

現時点では具体的なツールバージョンと環境構成を未確定としており、実装環境を作成していません。詳細設計とツール選定後に、このREADMEへ構築手順を追加します。

## ドキュメントの参照方法

- プロジェクト概要: `docs/project-overview.md`
- 開発方針: `docs/development-policy.md`
- 設計書一覧: `docs/README.md`
- 基本設計: `docs/basic-design/`
- 詳細設計テンプレート: `docs/templates/detailed-design-template.md`
- 横断設計: `docs/database/`、`docs/api/`、`docs/ui/`、`docs/test/`、`docs/operations/`

## 開発ルール

- 変更前に関連設計書を確認する。
- 設計・ソース・テスト間のトレーサビリティを維持する。
- 共通機能はCoreへ集約し重複実装しない。
- テナント境界、認証、権限、入力検証、監査を優先する。
- 未決定事項を推測で確定しない。
- 既存設計への影響を確認し、関連設計書を更新する。
- 未実装機能を実装済みとして記載しない。

共通ルールは `.github/copilot-instructions.md` を参照してください。

## 開発フェーズ

1. 基本設計
2. 詳細設計
3. 実装
4. 単体テスト
5. 結合テスト
6. 総合テスト
7. リリース・運用保守

要件定義書は作成しません。

## 今後の開発予定

次に、社員、組織、報告、ワークフローの機能詳細設計を作成し、DB・API・画面・テスト設計へ展開します。休暇申請、Wiki、タスク、案件、教育、評価、掲示板、議事録、AIはモジュール追加可能な将来機能として扱います。
