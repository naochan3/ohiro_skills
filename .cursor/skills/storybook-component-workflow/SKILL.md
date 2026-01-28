---
name: storybook-component-workflow
description: Storybookでコンポーネント駆動開発とドキュメント/テストを整備する手順。
---
# Storybook Component Workflow

## いつ使うか
- UIコンポーネントを分離して開発したい時
- デザインと実装の差分を減らしたい時
- a11y/ビジュアル回帰の検証を組み込みたい時

## 参照ルール（最優先）
- `.cursor/rules/06-component-driven-development.mdc`
- `.cursor/rules/10-frontend-quality-assurance.mdc`

## 要点（統合）
- コンポーネントを状態ごとにストーリー化する
- ドキュメント化は実装と同期させる
- a11yやビジュアル回帰をCIで回す

## 手順
1. Storybookを導入しフレームワーク設定
2. 主要コンポーネントの状態をストーリー化
3. Controls/Docsを整備し利用方法を明記
4. a11y/ビジュアル回帰テストを追加

## チェックリスト
- 主要状態（default/hover/focus/disabled/error）が揃っている
- Docsに使用例と注意点がある
- a11yチェックが実行できる
- ビジュアル回帰の基準が定義されている

## 出力テンプレ
1. 対象コンポーネント一覧
2. 状態一覧
3. Docsの要点
4. テスト設定
