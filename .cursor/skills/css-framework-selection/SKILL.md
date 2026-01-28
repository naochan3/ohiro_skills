---
name: css-framework-selection
description: CSSフレームワーク（Bootstrap/Tailwind）を導入・選定する手順。新規導入や移行判断時に使用。
metadata:
  sources:
    - https://github.com/twbs/bootstrap
    - https://github.com/tailwindlabs/tailwindcss
  license: MIT
---
# CSS Framework Selection

## いつ使うか
- 新規プロジェクトでCSSフレームワークを選定する時
- 既存プロジェクトのUI基盤を見直す時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **要件整理**: 速度重視か、デザイン自由度重視かを明確化
2. **現状把握**: 既存UI規約やTailwind運用の有無を確認
3. **候補比較**:
   - **Bootstrap**: 既成コンポーネント重視、導入が速い
   - **Tailwind**: カスタムデザイン重視、設計自由度が高い
4. **移行コスト評価**: 既存CSS/コンポーネントの再設計量を見積もる
5. **決定**: 採用理由と運用ルールを文書化

## チェックリスト
- 既存のデザインシステムと矛盾がない
- コンポーネント設計の一貫性を保てる
- チームの運用負荷が許容範囲

## 出力テンプレ
1. 選定対象
2. 採用フレームワーク
3. 採用理由（3点）
4. 運用ルール（命名/設計）
