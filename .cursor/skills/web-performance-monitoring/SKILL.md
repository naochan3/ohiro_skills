---
name: web-performance-monitoring
description: Core Web Vitalsの計測設計と分析フローを整備する。
---
# Web Performance Monitoring

## いつ使うか
- パフォーマンス計測を導入する時
- ボトルネックを可視化したい時

## 参照ルール（最優先）
- `.cursor/rules/25-performance-tuning.mdc`

## 要点
- CLS/INP/LCPをRUMで計測する
- attributionで原因を特定する
- 監視と改善サイクルを作る

## 手順
1. 計測対象とKPIを定義
2. web-vitalsでイベントを取得
3. 分析基盤へ送信（GA等）
4. 閾値判定と改善アクションを運用化

## 出力テンプレ
1. 計測対象/KPI
2. 計測方法
3. 送信先/可視化
4. 改善アクション
