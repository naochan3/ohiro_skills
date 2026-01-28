---
name: ismobilejs-usage
description: isMobile(ismobilejs) を使った端末判定を安全に実装する手順。UA判定が避けられない時に使用。
license: MIT
metadata:
  author: Kai Mallea
  source: https://github.com/kaimallea/isMobile
---
# isMobilejs Usage

## いつ使うか
- レスポンシブだけでは解決できない端末差分がある時
- サーバーサイドでUAベースの出し分けが必要な時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`
- `.cursor/skills/user-agent-detection/`

## 実行手順
1. **判定目的の明確化**: 「なぜUA判定が必要か」を短文で定義
2. **最小判定に絞る**: `phone/tablet/any` など粗い判定から開始
3. **サーバー/クライアント選定**: 可能ならサーバー側で判定
4. **フォールバック設計**: 判定が失敗した時のUIを用意
5. **計測**: 判定によるUI差分がUXを悪化させていないか確認

## 注意点
- UA文字列は不安定。判定は「最小限」に留める
- 可能なら **Client Hints** へ移行する
- リダイレクトや分岐は最小限にする

## 出力テンプレ
1. 判定目的
2. 判定粒度（any/phone/tablet）
3. 実装位置（Server/Client）
4. フォールバック
