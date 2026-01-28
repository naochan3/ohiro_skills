---
name: quicklink-prefetching
description: quicklinkでビューポート内リンクを安全にプリフェッチする手順。
license: Apache-2.0
metadata:
  author: GoogleChromeLabs
  source: https://github.com/GoogleChromeLabs/quicklink
---
# quicklink Prefetching
## いつ使うか
- MPAの次ページ体感速度を上げたい時
- 低コストでプリフェッチを導入したい時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`

## 実行手順
1. **対象範囲決定**: 観測対象のDOM範囲を決める
2. **除外設定**: 認証/課金/個人情報ページを除外する
3. **ネットワーク配慮**: Data Saverや低速回線への配慮を確認する
4. **オリジン制御**: 同一オリジンを基本に許可範囲を設定する
5. **計測**: LCP/INP/回遊率への影響を計測する

## チェックリスト
- 重要ページが除外されている
- 低速回線への配慮がある
- 体感速度の改善が確認できる

## 出力テンプレ
1. 観測対象
2. 除外条件
3. オリジン許可
4. 計測結果
