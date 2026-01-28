---
name: link-prefetching-optimization
description: 先読み（prefetch）方式を選定し、体感速度を改善する。
---
# Link Prefetching Optimization

## いつ使うか
- 次遷移の体感速度を上げたい時
- 先読みの負荷を制御したい時

## 参照ルール（最優先）
- `.cursor/rules/25-performance-tuning.mdc`

## 要点
- instant.pageは軽量で簡単
- quicklinkはviewport内リンクをアイドル時に先読み
- ネットワーク負荷とバッテリーを考慮

## 手順
1. 先読みの対象と条件を定義
2. ライブラリを選定
3. 設定（ignore/origins/threshold）
4. 計測と改善を実施

## チェックリスト
- 先読み対象が過剰でない
- 低速回線での負荷が許容
- 計測で効果確認済み

## 出力テンプレ
1. 先読み対象
2. 選定ライブラリ
3. 設定内容
4. 効果測定結果
