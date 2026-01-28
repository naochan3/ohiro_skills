---
name: state-management-patterns
description: ReduxとXStateの選択指針と導入手順を整理する。
---
# State Management Patterns

## いつ使うか
- 状態管理の選定/再設計を行う時
- 複雑なフローや状態遷移を扱う時

## 参照ルール（最優先）
- `.cursor/rules/05-react-patterns.mdc`

## 要点
- Reduxは予測可能なグローバル状態向け
- XStateは状態遷移が複雑なフロー向け
- どちらも「状態の責務」を明確にする

## 手順
1. 状態の種類と範囲を整理
2. Redux/XStateの適合度を評価
3. 最小構成で導入
4. デバッグ/テスト戦略を整備

## チェックリスト
- 状態の責務と所有者が明確
- 遷移が可視化されている
- テスト可能な単位に分割されている

## 出力テンプレ
1. 状態の分類
2. 選定理由
3. 実装スケッチ
4. テスト方針
