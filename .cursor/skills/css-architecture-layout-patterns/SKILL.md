---
name: css-architecture-layout-patterns
description: CSS設計（ITCSS）とレイアウト原則（Every Layout/Patterns）を統合し、JS不要のUIパターンまで整理する。
---
# CSS Architecture & Layout Patterns

## いつ使うか
- CSS設計方針の策定やリファクタリング
- レイアウト設計の体系化が必要なとき
- UIをJSなしで実現できるか検討する場面

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`
- `.cursor/rules/04-frontend-basics.mdc`
- `.cursor/rules/39-layout-and-responsive-strategy.mdc`

## 要点（統合）
- ITCSSでレイヤー順序を明確化し、詳細度を制御する
- レイアウトは「原理原則（コンテナ/スタック/クラスタ）」から組み立てる
- パターンは再利用前提で命名・構造化する
- JSを使わないUIはアクセシビリティ優先で設計する

## 手順
1. ITCSSの層（Settings/Tools/Generic/Elements/Objects/Components/Utilities）を決める
2. レイアウトを原理パターン（Stack/Cluster/Sidebar/Switcher等）で設計
3. パターンに名前と責務を与え、使い回し可能にする
4. JS不要で実現できる挙動はCSS優先で設計

## チェックリスト
- レイヤーの依存関係が逆転していない
- レイアウトはユーティリティ/オブジェクトで再利用可能
- パターンは単体で説明できる責務になっている
- JSが不要な場合はCSSで実装している
- フォーカス/キーボード操作の配慮がある

## 出力テンプレ
1. ITCSSレイヤー構成
2. レイアウト原理の選定（なぜそのパターンか）
3. パターン一覧（責務/利用箇所）
4. JS不要で代替できる挙動
