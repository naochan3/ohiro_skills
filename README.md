# Ohiro Skills Collection

Cursor IDE用のカスタムスキル（Agent Skills）コレクションです。

## 概要

このリポジトリには、開発効率を向上させるための様々なスキルが含まれています。各スキルは特定のタスクや技術領域に特化しており、Cursor AIエージェントが適切なタイミングで自動的に参照・活用します。

## スキル一覧

※以下は主要スキルの概要です。完全な一覧は `.cursor/skills/` を参照してください。

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
| `state-management-patterns` | React 状態管理パターン |
| `threejs-react-workflow` | Three.js + React のワークフロー |
| `every-layout-patterns` | Every Layout のレイアウトプリミティブ活用 |
| `modern-css-solutions` | CSSだけで解決するUIパターンの選定 |
| `css-framework-selection` | CSSフレームワーク選定（Bootstrap/Tailwind） |
| `open-props-design-tokens` | Open Props デザイントークンの導入 |
| `css-without-js-patterns` | JS不要のCSS UIパターン検討 |
| `ismobilejs-usage` | isMobileによる端末判定の安全運用 |
| `ua-parser-js-usage` | UAParser.jsの導入判断と運用 |
| `ua-client-hints-usage` | User Agent Client Hintsの運用 |
| `bowser-usage` | Bowserによるブラウザ判定 |
| `detect-it-usage` | 入力デバイス特性の判定 |
| `responsively-testing-workflow` | Responsively Appによるレスポンシブ検証 |
| `playwright-e2e-testing` | Playwright E2Eテスト設計 |
| `css-specs-reference` | CSS仕様参照と実装判断 |
| `css-env-safe-area` | safe-area対応（iOSノッチ） |
| `webdev-best-practices` | web.devベストプラクティス確認 |

### 🏗️ アーキテクチャ・設計

| スキル | 説明 |
|--------|------|
| `api-design-guidelines` | API 設計ガイドライン |
| `architecture-implementation-guide` | アーキテクチャ実装ガイド |
| `system-design-and-adr` | システム設計と ADR（Architecture Decision Records） |
| `event-driven-microservices-playbook` | イベント駆動マイクロサービスのプレイブック |
| `itcss-architecture` | ITCSSレイヤ設計によるCSS整理 |
| `design-principles-application` | 設計原則/法則の統合判断 |
| `css-architecture-layout-patterns` | CSS設計とレイアウト原則の統合 |
| `design-system-generator-and-validator` | デザインシステム推定と検証 |
| `react-production-ready-guide` | 本番品質のReact設計ガイド |
| `graphql-schema-design` | GraphQLスキーマ設計と運用 |

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
| `storybook-component-workflow` | Storybook コンポーネント開発ワークフロー |
| `web-performance-monitoring` | Core Web Vitals 計測設計 |
| `instantpage-prefetch` | instant.page による事前取得 |
| `quicklink-prefetching` | quicklink による事前取得 |

### 🔐 セキュリティ

| スキル | 説明 |
|--------|------|
| `web-security-audit` | Web セキュリティ監査 |
| `oauth-2-1-security` | OAuth 2.1 セキュリティ実装 |
| `zero-trust-architecture-basics` | ゼロトラストアーキテクチャの基礎 |
| `user-agent-detection` | UA/Client Hints の判定方針 |

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
| `figma-implement-design` | Figma デザインをコードに変換（MCP連携、1:1ビジュアル再現） |
| `frontend-design` | 高品質なフロントエンドデザインの設計・実装 |
| `web-design-guidelines` | UI/UX とアクセシビリティ観点でのレビュー |
| `webapp-testing` | ローカル Web アプリの手動/自動検証 |
| `motion-and-scrollytelling` | モーション・スクロールアニメーション |
| `link-prefetching-optimization` | リンクプリフェッチ最適化 |
| `responsive-resources-curation` | レスポンシブUI参考パターンの収集・評価 |
| `mobile-first-strategy` | モバイルファースト設計 |
| `uiux-resource-catalog` | UI/UX素材・ツールの探索と選定 |
| `uiux-principles-synthesis` | UI/UXの原則と品質チェック |
| `lp-uiux-frontend-flow` | LP/UIUX/Frontendの作業フロー |
| `page-transitions-strategy` | ページ遷移方式の選定 |
| `barba-page-transitions` | Barba.jsのページ遷移設計 |
| `swup-page-transitions` | Swupのページ遷移設計 |
| `view-transitions-api` | View Transitions APIの段階導入 |
| `iframe-resizer-integration` | iframe-resizer導入とサイズ同期 |

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
| `learning-path-and-skill-catalog` | 学習ロードマップとスキル棚卸し |

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
