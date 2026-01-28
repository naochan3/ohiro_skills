---
name: detect-it-usage
description: detect-itで入力デバイス特性を判定しUXを最適化する手順。
license: MIT
metadata:
  author: rafgraph
  source: https://github.com/rafgraph/detect-it
---
# detect-it Usage
## いつ使うか
- mouse/touch/hybridの入力差分でUXを調整したい時
- Pointer Events対応の有無を判定して実装を切り替えたい時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **目的整理**: 入力差分で変えたいUIを特定する
2. **判定対象の決定**: `deviceType` / `primaryInput` / `supportsPointerEvents` を選ぶ
3. **UX最適化**: 入力に合わせたUI微調整を設計する
4. **互換性フォールバック**: 判定失敗時の既定挙動を決める
5. **検証**: 主要デバイスでタッチ/マウス双方の操作性を確認する

## チェックリスト
- 入力差分の目的が明確
- どの入力でも操作できる
- 判定に依存した致命的分岐が無い

## 出力テンプレ
1. 変更対象UI
2. 使用する判定
3. フォールバック
