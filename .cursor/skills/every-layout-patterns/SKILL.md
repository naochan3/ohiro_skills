---
name: every-layout-patterns
description: Every Layoutのレイアウトプリミティブを参考に、ページ構成を組み立てる手順。
metadata:
  author: Every Layout
  source: https://github.com/EveryLayout/every-layout
  source_note: README取得に失敗したため一般原則に基づく
license_note: リポジトリ内LICENSEの確認が必要
---
# Every Layout Patterns
## いつ使うか
- レイアウト設計をコンポーネント化して再利用したい時
- Grid/Flexの使い分けが曖昧で一貫性が崩れている時
- UIの余白や整列ルールを最小限の抽象でまとめたい時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **画面の目的整理**: 情報の階層（主要/補助/詳細）を明確にする
2. **プリミティブ選定**: Stack/Cluster/Sidebar/Center などの基本レイアウトに分類する
3. **間隔ルール定義**: 8pxグリッド基準で余白を統一する
4. **CSS変数化**: 可変寸法（gap, max-width 等）を変数で管理する
5. **再利用単位の確定**: 1レイアウト=1責務の粒度に揃える

## チェックリスト
- レイアウトがコンテンツの意味に沿っている
- 余白と整列のルールが画面間で一致している
- 1コンポーネント内で複数のレイアウト責務が混ざっていない

## 出力テンプレ
1. 対象画面
2. 選定したプリミティブ
3. 主要レイアウト変数（gap, max-width 等）
4. 再利用方針
