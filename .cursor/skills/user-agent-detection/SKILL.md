---
name: user-agent-detection
description: UA文字列とClient Hintsを使った環境判定の方針を整理する。
---
# User Agent Detection

## いつ使うか
- ブラウザ/端末差分を安全に扱う必要がある時
- UA文字列依存を減らしたい時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`

## 要点
- UA文字列解析は最小限にする
- 可能ならClient Hintsへ移行する
- 判定ロジックはホワイトリスト寄りで設計

## 手順
1. 必要な判定条件を最小化
2. UAライブラリ（ua-parser/bowser）を選定
3. Client Hintsが使える環境は移行
4. 判定結果の影響範囲を限定

## チェックリスト
- 判定理由が明確
- UA文字列への依存が最小
- Client Hintsの許可ヘッダーが設定済み

## 出力テンプレ
1. 判定目的
2. 判定方式（UA/Client Hints）
3. 実装方針
4. リスクと代替
