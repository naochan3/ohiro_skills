---
name: responsively-testing-workflow
description: Responsively App を使ったレスポンシブ検証手順。多端末同時レビューが必要な時に使用。
license: AGPL-3.0
metadata:
  author: responsively-org
  source: https://github.com/responsively-org/responsively-app
---
# Responsively Testing Workflow

## いつ使うか
- 多端末プレビューを同時に確認したい時
- レスポンシブ崩れの早期検出が必要な時

## 実行手順
1. **デバイス条件の整理**: 主要ターゲット（幅/OS/ブラウザ）を決める
2. **レイアウト設定**: プレビューの並び・サイズを調整する
3. **主要フロー検証**: 重要導線を一通り操作して崩れを確認
4. **スクリーンショット**: 問題点を記録する
5. **差分整理**: 修正対象の優先順位を付ける

## チェックリスト
- 最小幅で致命的な崩れが無い
- 重要CTAが隠れない
- 文字サイズ/行間が読める

## 出力テンプレ
1. 対象ページ
2. デバイス構成
3. 問題点
4. 優先度
