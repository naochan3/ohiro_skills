---
name: ua-parser-js-usage
description: UAParser.jsを使ったUA解析の導入判断と安全運用の手順。
license: AGPL-3.0
metadata:
  author: faisalman
  source: https://github.com/faisalman/ua-parser-js
  docs: https://docs.uaparser.dev
  license_note: v2系はAGPLのため利用条件に注意
---
# UAParser.js Usage
## いつ使うか
- 端末/ブラウザ差分の回避策が必要な時
- どうしてもUA解析が避けられない要件がある時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`
- `.cursor/skills/user-agent-detection/`

## 実行手順
1. **必要性判断**: Feature DetectionやUA-CHで代替できないか確認する
2. **利用範囲の最小化**: 解析対象は必要最小限の項目に限定する
3. **実装位置の決定**: Server/Clientのどちらで解析するか決める
4. **マッピング設計**: 解析結果は「機能差分」に変換して使う
5. **ログと監査**: UAの保存は最小限にし、機密扱いにする

## 注意点
- AGPLの適用範囲を確認し、必要なら商用ライセンスを検討する
- UAは偽装され得るため、判定は絶対条件にしない

## チェックリスト
- UA解析の必然性が説明できる
- 判定結果に依存した破壊的分岐が無い
- 収集/保存のポリシーが定義されている

## 出力テンプレ
1. UA解析が必要な理由
2. 解析項目
3. 実装位置（Server/Client）
4. フォールバック
