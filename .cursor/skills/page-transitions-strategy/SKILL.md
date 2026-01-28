---
name: page-transitions-strategy
description: ページ遷移の方式選定（MPA/SPA/ネイティブAPI）と実装手順を整理する。
---
# Page Transitions Strategy

## いつ使うか
- 画面遷移の体験を強化したい時
- MPA/SPAの方式選定が必要な時

## 参照ルール（最優先）
- `.cursor/rules/01-design-system.mdc`
- `.cursor/rules/25-performance-tuning.mdc`

## 要点
- MPAならBarba/Swupで遷移演出を追加
- ネイティブView Transitions APIを検討
- React Routerはルーティング設計の基盤
- iframeはサイズ/スクロール同期に注意

## 手順
1. ルーティング方式を決定（MPA/SPA）
2. 遷移の目的と演出範囲を定義
3. ライブラリ/APIを選定
4. パフォーマンスとアクセシビリティを確認

## チェックリスト
- 遷移がUXを阻害していない
- 遷移演出が軽量である
- ルーティング責務が分離されている
- iframeはリサイズ/セキュリティ設定がある

## 出力テンプレ
1. 方式選定
2. ライブラリ/API選定理由
3. 遷移範囲
4. リスクと対策
