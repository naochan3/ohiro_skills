---
name: css-env-safe-area
description: CSS Environment Variables（safe-area）を使ったノッチ対応の実装手順。iOS対応やフルスクリーンUIで使用。
metadata:
  author: W3C CSS Working Group
  source: https://github.com/w3c/csswg-drafts/tree/main/css-env-1
  license_note: リポジトリのライセンス表記は要確認
---
# CSS Env Safe Area

## いつ使うか
- iOSのノッチ/ホームインジケータを考慮したい時
- フルスクリーンUIで余白が必要な時

## 実行手順
1. **対象領域の特定**: どのコンテナが安全領域に被るかを把握
2. **CSS変数の適用**: `env(safe-area-inset-*)` を使用
3. **フォールバック**: `env()` 未対応ブラウザ向けに既定値を入れる
4. **検証**: 実機/エミュレータで余白が適切か確認

## 例（最小）
```css
.safe-area {
  padding-top: max(16px, env(safe-area-inset-top));
  padding-right: max(16px, env(safe-area-inset-right));
  padding-bottom: max(16px, env(safe-area-inset-bottom));
  padding-left: max(16px, env(safe-area-inset-left));
}
```

## チェックリスト
- 重要UIがノッチに被らない
- 余白が過剰になっていない
- 端末ごとの差分が許容範囲
