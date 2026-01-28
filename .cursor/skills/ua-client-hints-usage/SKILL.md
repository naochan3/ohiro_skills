---
name: ua-client-hints-usage
description: User Agent Client Hints(UA-CH)を使った安全な端末情報取得手順。
metadata:
  author: WICG
  source: https://github.com/WICG/ua-client-hints
  license: W3C Software and Document License
---
# UA Client Hints Usage
## いつ使うか
- UA解析を減らし、ヒントヘッダーで情報を取得したい時
- 端末の高エントロピー情報を最小限に扱いたい時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`
- `.cursor/skills/user-agent-detection/`

## 実行手順
1. **低エントロピー優先**: `Sec-CH-UA` と `Sec-CH-UA-Mobile` など最低限から使う
2. **Accept-CH設計**: 必要なヒントだけを `Accept-CH` で要求する
3. **SecureContext前提**: HTTPSでのみ取得できる前提で設計する
4. **JS API活用**: `navigator.userAgentData` で必要な値だけ取得する
5. **フォールバック**: UA-CH非対応時の挙動を定義する

## 注意点
- 高エントロピー情報は取得理由を明文化する
- 取得情報は保存を最小限にし、目的外利用をしない

## チェックリスト
- Accept-CHの要求範囲が最小
- 非対応環境のフォールバックがある
- 取得データの保管ポリシーが定義済み

## 出力テンプレ
1. 取得したいヒント
2. Accept-CHの設定
3. フォールバック
4. 保存/利用方針
