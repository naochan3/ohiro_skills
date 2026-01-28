---
name: monitoring-observability
description: 監視・可観測性の設計と実装手順。メトリクス/ログ/トレース/アラート/SLOの整備時に使用。
license: MIT
metadata:
  author: ahmedasmar
  source: https://github.com/ahmedasmar/devops-claude-skills
---

# Monitoring & Observability

監視と可観測性を整えるための実行手順です。

## いつ使うか

- 監視の設計をやり直す時
- 障害の原因が掴めない時
- SLO/アラート設計を整備したい時

## 実行手順

1. **ゴール整理**: 重要ユーザーフローとSLOを定義する。
2. **メトリクス設計**:
   - Golden Signals（Latency/Traffic/Errors/Saturation）
   - RED/USEのどちらを軸にするか決める
3. **ログ設計**:
   - 構造化ログ + リクエストID
   - PIIのマスキングと保持期間の決定
4. **トレース導入**:
   - OpenTelemetryで主要フローを計測
   - サンプリング戦略を設定
5. **アラート設計**:
   - 症状ベースのアラート
   - ノイズ削減とRunbook整備
6. **ダッシュボード設計**:
   - 重要指標を上部に集約
   - 同一時間軸で比較
7. **継続改善**:
   - インシデント後の振り返り
   - 誤検知/不足検知の改善

## 参照

- https://github.com/ahmedasmar/devops-claude-skills
