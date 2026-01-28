# Ohiro Skills Collection

Cursor IDE用のカスタムスキル（Agent Skills）コレクションです。

## 概要

このリポジトリには、開発効率を向上させるための様々なスキルが含まれています。各スキルは特定のタスクや技術領域に特化しており、Cursor AIエージェントが適切なタイミングで自動的に参照・活用します。

## スキル一覧

### 📦 フレームワーク・ライブラリ

| スキル | 説明 |
|--------|------|
| `next-best-practices` | Next.js のベストプラクティス（RSC、データパターン、メタデータ、エラーハンドリング等） |
| `next-cache-components` | Next.js 16 のキャッシュコンポーネント（PPR、use cache、cacheLife等） |
| `next-upgrade` | Next.js のアップグレード手順 |
| `vercel-react-best-practices` | React/Next.js の性能最適化 |
| `vercel-react-native-skills` | React Native/Expo の性能・UX最適化 |
| `vercel-composition-patterns` | React のコンポジション設計パターン |
| `supabase-postgres-best-practices` | Supabase/Postgres のベストプラクティス |

### 🛠️ 開発ツール・インフラ

| スキル | 説明 |
|--------|------|
| `docker-best-practices` | Dockerfile を安全かつ軽量に作成 |
| `deployment-paas` | Vercel/Railway など PaaS へのデプロイ |
| `gcp-cloud-run-deployment` | Cloud Run へのデプロイ自動化 |
| `ci-cd` | CI/CD パイプライン設計・最適化 |
| `monitoring-observability` | 監視・可観測性の設計と実装 |
| `varlock` | 環境変数/シークレットの安全な管理 |
| `mcp-builder` | MCP サーバーの設計・実装・検証 |

### 📝 ドキュメント・レビュー

| スキル | 説明 |
|--------|------|
| `doc-coauthoring` | 仕様書/提案書/設計書の共著 |
| `bmad-index-docs` | ディレクトリのドキュメント索引生成 |
| `bmad-shard-doc` | 大きな Markdown の分割と索引生成 |
| `bmad-editorial-review-prose` | 文章の可読性・明確さの校正 |
| `bmad-editorial-review-structure` | 文書構成の改善提案 |
| `bmad-review-adversarial` | 仕様・差分の懐疑的レビュー |
| `learning-documentation` | プロジェクトの学習ドキュメント作成 |

### 🎨 デザイン・UI/UX

| スキル | 説明 |
|--------|------|
| `frontend-design` | 高品質なフロントエンドデザインの設計・実装 |
| `web-design-guidelines` | UI/UX とアクセシビリティ観点でのレビュー |
| `webapp-testing` | ローカル Web アプリの手動/自動検証 |

### 🚀 ワークフロー・プロジェクト管理

| スキル | 説明 |
|--------|------|
| `solo-dev-workflow` | ソロ開発の立ち上げと運用効率化 |
| `rule-bootstrap` | 新規プロジェクトのルール環境構築 |
| `requirements-definition` | 要件が曖昧な場合の整理手順 |
| `project-memory` | 重要な意思決定の短期記憶ログ記録 |
| `static-to-dynamic` | 静的 UI を動的アプリへ変換 |
| `skill-creator` | 新規スキルの定義・構成・検証 |
| `web-scraping` | 倫理的かつ堅牢な Web スクレイピング |

## 使い方

### Cursor IDE での利用

1. このリポジトリを `.cursor/skills/` ディレクトリにクローンまたはコピー
2. Cursor IDE がスキルを自動的に認識
3. 関連するタスクを実行する際、エージェントが適切なスキルを参照

### スキルの構造

各スキルは以下の構造を持ちます：

```
skill-name/
├── SKILL.md          # メインのスキル定義ファイル
└── *.md              # 補足ドキュメント（必要に応じて）
```

## ライセンス

Private - 個人利用

## 作者

Hironao Ishioka (石岡 大尚)
