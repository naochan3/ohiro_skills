---
name: playwright-e2e-testing
description: Playwright を使ったE2Eテストの設計と運用手順。UIの自動検証や回帰テスト時に使用。
license: Apache-2.0
metadata:
  author: Microsoft
  source: https://github.com/microsoft/playwright
---
# Playwright E2E Testing

## いつ使うか
- UIの回帰テストを自動化したい時
- クロスブラウザ検証が必要な時

## 実行手順
1. **対象フロー定義**: 重要ユーザーフローを選定
2. **テスト設計**: 1テスト=1目的、冪等性を保つ
3. **選択子設計**: 安定した `data-testid` を優先
4. **実行/トレース**: 失敗時はTrace Viewerで原因特定
5. **CI連携**: 最低限のスモークテストをCIに組み込む

## チェックリスト
- テストが環境に依存しない
- 画像/動画のゴールデン更新ルールが明確
- リトライは必要最小限

## 出力テンプレ
1. 対象フロー
2. テストケース
3. 必要なテストデータ
4. CI方針
