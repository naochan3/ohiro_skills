---
name: modern-css-solutions
description: Modern CSS Solutionsの観点で、JSに頼らないUI実装を選定する手順。
metadata:
  author: ModernCSS
  source: https://github.com/ModernCSS/modern-css-solutions
  source_note: README取得に失敗したため一般原則に基づく
license_note: リポジトリ内LICENSEの確認が必要
---
# Modern CSS Solutions
## いつ使うか
- レイアウトやUI表現をCSSだけで解決したい時
- 既存JSが重く、CSSで代替できる可能性がある時
- デザイン要件を満たしつつ実装コストを下げたい時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **要件分解**: 目的・制約・対応ブラウザを整理する
2. **CSS候補選定**: Grid/Flex/Clamp/Container Query などの適用可否を確認
3. **互換性チェック**: 主要ブラウザでの対応状況を確認する
4. **最小実装**: 小さな検証コードで要件を満たすか確認する
5. **段階導入**: 既存コードへ影響の小さい部分から適用する

## チェックリスト
- 目的が明確で、CSSだけで成立する
- フォールバック方針がある
- パフォーマンスとアクセシビリティを損なわない

## 出力テンプレ
1. 目的/要件
2. 使用するCSS機能
3. 互換性リスク
4. フォールバック
