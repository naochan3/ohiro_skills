---
name: view-transitions-api
description: View Transitions APIの段階導入とフォールバック設計の手順。
metadata:
  author: WICG
  source: https://github.com/WICG/view-transitions
  license: W3C Software and Document License
---
# View Transitions API
## いつ使うか
- ページ遷移の認知負荷を下げたい時
- SPA/MPAで共通の遷移表現を検討する時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **対応状況確認**: 対象ブラウザのサポート範囲を把握する
2. **遷移対象の選定**: 画面全体か要素単位かを決める
3. **段階導入**: View Transitions非対応時のCSSフォールバックを設計する
4. **動線確認**: 遷移が情報理解を助けるか検証する
5. **低負荷設計**: `prefers-reduced-motion` に配慮する

## チェックリスト
- フォールバックが用意されている
- 遷移の目的が明確
- 速度/可読性を損なわない

## 出力テンプレ
1. 対象遷移
2. API利用方針
3. フォールバック
4. 検証項目
