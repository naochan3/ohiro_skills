---
name: itcss-architecture
description: ITCSSのレイヤ設計でCSSを整理し、拡張性と予測可能性を高める手順。
metadata:
  author: ITCSS
  source: https://github.com/itcss/itcss
  source_note: README取得に失敗したため一般原則に基づく
license_note: リポジトリ内LICENSEの確認が必要
---
# ITCSS Architecture
## いつ使うか
- CSSが肥大化して依存関係が追えない時
- 影響範囲の予測が難しく、修正が怖い時
- コンポーネント設計の責務分離が必要な時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **レイヤ定義**: Settings/Tools/Generic/Elements/Objects/Components/Utilities を整理
2. **依存方向の明示**: 上層から下層への依存のみ許可する
3. **命名規則の統一**: BEMやユーティリティ命名を層ごとに整理する
4. **移行計画**: 既存CSSを小さな単位でレイヤへ移す
5. **検証**: 影響範囲の可視化と回帰確認を行う

## チェックリスト
- レイヤ間の依存が一方向になっている
- 共通設定（色、間隔）が上位レイヤに集約されている
- 例外的な上書きがUtilitiesに閉じている

## 出力テンプレ
1. レイヤ構成
2. 既存CSSの移行順序
3. 命名規則
4. 影響範囲の確認方法
