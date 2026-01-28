---
name: barba-page-transitions
description: Barba.jsでマルチページ遷移をスムーズにする実装手順。
license: MIT
metadata:
  author: Barba.js
  source: https://github.com/barbajs/barba
  docs: https://barba.js.org
---
# Barba Page Transitions
## いつ使うか
- MPAでページ遷移を滑らかにしたい時
- 遷移中のUXやローディング体験を改善したい時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`
- `.cursor/rules/23-security-policy.mdc`

## 実行手順
1. **DOM構造整理**: 主要コンテナと遷移対象の範囲を決める
2. **遷移設計**: leave/enterの基本アニメーションとタイミングを定義する
3. **ビュー分割**: ページ固有処理をView単位に整理する
4. **状態管理**: スクロール位置やメタ情報の更新方針を決める
5. **フォールバック**: JS無効時でも崩れない構成を維持する

## チェックリスト
- 遷移対象が限定されている
- 画面固有ロジックが混在していない
- アクセシビリティの配慮がある

## 出力テンプレ
1. 遷移対象コンテナ
2. 遷移アニメーション方針
3. View分割
4. フォールバック
