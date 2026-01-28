---
name: css-without-js-patterns
description: JSを使わずにCSSで実現できるUI表現を検討する手順。軽量化やアクセシビリティ優先時に使用。
license: GPL-3.0
metadata:
  author: you-dont-need
  source: https://github.com/you-dont-need/You-Dont-Need-JavaScript
  note: GPL-3.0のため、具体コードの転載は行わない
---
# CSS Without JS Patterns

## いつ使うか
- JS削減でパフォーマンスを上げたい時
- CSSだけで実現できる表現を探したい時
- 小さなUI挙動（トグル、アコーディオン等）を最小実装したい時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`
- `.cursor/rules/23-security-policy.mdc`

## 実行手順
1. **UI要件の整理**: 何を動かしたいかを簡潔に定義
2. **CSSで可能か評価**: `:checked`/`details`/`@keyframes` などの活用余地を確認
3. **アクセシビリティ確認**: キーボード操作/フォーカス/読み上げを検討
4. **最小実装**: JSを使わずに成立する最小構成を試す
5. **限界判断**: 要件を満たせない場合のみJSを追加

## チェックリスト
- キーボード操作で利用できる
- 状態が視覚的に分かる
- `prefers-reduced-motion` に配慮

## 出力テンプレ
1. CSSで実現する対象
2. 使うCSS機能（例: details/summary）
3. 期待する挙動
4. JSが必要な場合の理由
