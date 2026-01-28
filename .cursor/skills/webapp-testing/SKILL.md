---
name: webapp-testing
description: ローカルWebアプリを手動/自動で検証する手順。UIの動作確認、スクリーンショット、DOM検査に使用。
license: Apache-2.0
metadata:
  author: Anthropic
  source: https://github.com/anthropics/skills
---

# Web Application Testing

ローカルWebアプリを安全に確認・検証するための手順です。

## いつ使うか

- UIの動作確認や回帰チェック
- DOM構造の把握が必要なとき
- クリック/入力などの一連操作を再現したいとき

## 実行手順

1. **環境確認**: アプリの起動方法・URL・認証要件を把握する。
2. **起動確認**: サーバが動いていない場合は起動する（ログは必要最小限）。
3. **手動確認**:
   - 画面遷移、フォーム送信、エラー表示を確認
   - 重要導線は最低1回通す
4. **自動確認（必要時）**:
   - Playwright等で再現スクリプトを作成
   - `networkidle` 等の待機で描画完了を保証
   - 取得したセレクタで操作を実行
5. **証跡**:
   - スクリーンショットや要約ログを残す
   - 失敗時は再現手順と期待/実結果を記録

## 注意点

- 動的UIは**描画完了後**にDOMを取得する
- セレクタは `role` や `data-testid` を優先
- 可能なら自動化は小さく段階的に実施

## 参照

- https://github.com/anthropics/skills
