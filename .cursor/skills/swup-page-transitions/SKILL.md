---
name: swup-page-transitions
description: Swupでページ遷移、キャッシュ、プリロードを設計する手順。
license: MIT
metadata:
  author: swup
  source: https://github.com/swup/swup
  docs: https://swup.js.org
---
# Swup Page Transitions
## いつ使うか
- MPAの遷移をSPA風にしたい時
- プリロードやキャッシュで体感速度を上げたい時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`
- `.cursor/rules/23-security-policy.mdc`

## 実行手順
1. **対象範囲決定**: Swupが管理するコンテナを明確化する
2. **遷移設計**: CSS遷移/アニメーションの基準を作る
3. **プラグイン選定**: progress/head/scrollなど必要な機能を選ぶ
4. **キャッシュ方針**: どのページをキャッシュするか決める
5. **アクセシビリティ確認**: フォーカス管理と履歴更新を確認する

## チェックリスト
- 遷移範囲が限定されている
- 主要プラグインの採用理由がある
- 既存の履歴/メタ更新と競合しない

## 出力テンプレ
1. 管理コンテナ
2. 遷移方針
3. 採用プラグイン
4. キャッシュ方針
