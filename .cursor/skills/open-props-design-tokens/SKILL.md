---
name: open-props-design-tokens
description: Open Props のデザイン・トークンを評価・導入する手順。CSS変数設計や試作時に使用。
license: MIT
metadata:
  author: Adam Argyle
  source: https://github.com/argyleink/open-props
---
# Open Props Design Tokens

## いつ使うか
- CSS変数を体系化したい時
- デザイントークンの試作が必要な時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **用途整理**: どのカテゴリ（色/影/タイポ/サイズ）を使うか決める
2. **影響範囲確認**: 既存のCSS変数やTailwind設定と衝突しないか確認
3. **導入方式**: CDN かローカル取り込みかを決める
4. **マッピング**: Open Props → 既存トークンに対応付ける
5. **検証**: コントラスト/一貫性/運用性を確認

## チェックリスト
- 既存トークンと衝突しない
- アクセシビリティ基準を満たす
- 運用ルールが明文化されている

## 出力テンプレ
1. 使用カテゴリ
2. 導入方式（CDN/ローカル）
3. 既存トークンとの対応
4. 注意点
