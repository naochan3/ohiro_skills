---
name: css-specs-reference
description: CSS仕様（csswg-drafts）を参照して仕様確認・実装判断を行う手順。新しいCSS機能導入時に使用。
metadata:
  author: W3C CSS Working Group
  source: https://github.com/w3c/csswg-drafts
  license_note: リポジトリのライセンス表記は要確認
---
# CSS Specs Reference

## いつ使うか
- 新しいCSS機能を使うか迷う時
- 仕様や構文の厳密さが必要な時

## 実行手順
1. **対象仕様の特定**: 使いたい機能の仕様名を特定
2. **安定性確認**: Editor’s Draft / WD / CR など成熟度を確認
3. **互換性確認**: 実装状況を調べ、フォールバックを設計
4. **最小実装**: 最小の検証コードで動作確認
5. **本実装**: 互換性と運用性を考慮して適用

## チェックリスト
- フォールバックが用意されている
- アクセシビリティが損なわれない
- 仕様変更リスクが許容範囲

## 出力テンプレ
1. 使用するCSS機能
2. 仕様の成熟度
3. 互換性リスク
4. フォールバック
