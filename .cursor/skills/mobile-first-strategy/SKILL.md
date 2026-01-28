---
name: mobile-first-strategy
description: モバイルファーストで情報設計とレイアウトを設計するための手順。新規画面設計やレスポンシブ設計時に使用。
metadata:
  author: Brad Frost
  source: https://github.com/bradfrost/mobile-first
  source_note: README取得に失敗したため内容は一般原則に基づく
  license_note: リポジトリのライセンス表記は要確認
---
# Mobile-First Strategy

## いつ使うか
- 新規UIをレスポンシブ対応で設計する時
- 情報の優先順位を再設計する時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **目的と主要タスクの整理**: 小さい画面で必須の要素だけを抽出する
2. **情報の階層化**: 主要/補助/詳細に分け、モバイルでは主要を優先
3. **最小UI設計**: 1画面の焦点を1つに絞る
4. **拡張設計**: `min-width` で段階的に情報/機能を追加する
5. **検証**: 320px〜の最小幅で視認性/操作性を確認する

## チェックリスト
- 小画面で完結する主要導線がある
- タップ領域は 44px 以上
- 余白と行間が詰まりすぎていない
- `min-width` の拡張は段階的

## 出力テンプレ
1. 主要タスク
2. モバイル最小構成
3. ブレークポイントごとの追加要素
4. 重要なUI制約
