---
name: web-design-guidelines
description: UI/UXとアクセシビリティ観点でのレビュー手順。UIレビューやデザイン監査の依頼時に使用。
license: MIT
metadata:
  author: Vercel
  source: https://github.com/vercel-labs/agent-skills
  guidelines: https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md
---

# Web Design Guidelines

UIコードをレビューするためのチェック手順をまとめたスキルです。  
**このプロジェクトのデザインルールが最優先**であり、外部ガイドラインは補助として扱います。

## いつ使うか

- 「UIレビューして」「アクセシビリティ見て」などの依頼
- デザイン実装の品質確認

## 実行手順

1. **対象範囲の確認**: レビュー対象ファイルや画面を特定する。
2. **プロジェクト内ルールの優先適用**:
   - `01-design-system.mdc` と関連ルールに必ず従う
3. **外部ガイドラインの参照**:
   - 必要なら `guidelines` のURLから最新ガイドを取得
4. **レビュー観点**:
   - アクセシビリティ（コントラスト/フォーカス/キーボード操作）
   - レイアウト/余白/視線誘導
   - 状態設計（hover/active/disabled/loading/error）
   - タイポグラフィ（階層/サイズ/行間）
   - 画像/アイコンの品質
   - モバイル最適化（タップ領域/レスポンシブ）
5. **指摘の出力**:
   - 問題箇所と理由、改善案をセットで提示

## 参照

- https://github.com/vercel-labs/agent-skills
- https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md
