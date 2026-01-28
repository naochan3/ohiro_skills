---
name: instantpage-prefetch
description: instant.pageでホバー/タッチ時の事前取得を導入する手順。
license: MIT
metadata:
  author: instant.page
  source: https://github.com/instantpage/instant.page
  docs: https://instant.page
---
# instant.page Prefetch
## いつ使うか
- MPAの体感速度を簡易的に改善したい時
- ユーザー操作直前に安全にプリフェッチしたい時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`

## 実行手順
1. **対象ページ選定**: 主要導線のみ適用する
2. **除外ルール設計**: 認証/購入/個人情報ページは除外する
3. **読み込み位置決定**: クリティカルCSS後にスクリプトを配置する
4. **計測**: 体感速度の変化を計測する
5. **監視**: 予期せぬプリフェッチをログで監視する

## チェックリスト
- 重要ページの除外ができている
- プリフェッチ対象が明確
- 速度改善の効果が確認できる

## 出力テンプレ
1. 対象導線
2. 除外ルール
3. 計測結果
