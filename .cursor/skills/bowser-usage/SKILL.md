---
name: bowser-usage
description: Bowserでブラウザ/OS/プラットフォーム判定を行う導入手順。
license: MIT
metadata:
  author: bowser-js
  source: https://github.com/lancedikson/bowser
---
# Bowser Usage
## いつ使うか
- 互換性問題の回避でブラウザ判定が必要な時
- サポート対象の最小要件を判定したい時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`
- `.cursor/skills/user-agent-detection/`

## 実行手順
1. **必要性の確認**: 可能ならFeature Detectionを優先する
2. **解析方法の選定**: `getParser` または `parse` の使い分けを決める
3. **判定条件の定義**: `satisfies()` で必要最小限の条件を作る
4. **フォールバック**: 未判定や偽装UAに備えた既定挙動を用意する
5. **計測**: 判定によるUX影響をモニタリングする

## チェックリスト
- 判定は最小限の条件に限定している
- 失敗時の挙動が安全側になっている
- 解析結果の保存が最小限になっている

## 出力テンプレ
1. 判定目的
2. 判定条件
3. フォールバック
