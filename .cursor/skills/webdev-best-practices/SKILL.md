---
name: webdev-best-practices
description: web.dev の知見をベースに、パフォーマンス/アクセシビリティ/UXを改善するための確認手順。
metadata:
  author: GoogleChrome
  source: https://github.com/GoogleChrome/web.dev
  license_note: コンテンツは CC BY 3.0 / コードサンプルは Apache-2.0
---
# web.dev Best Practices

## いつ使うか
- WebパフォーマンスやUXの改善タスク
- アクセシビリティ対応が必要な時
- Web標準の最新ベストプラクティスを確認したい時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`
- `.cursor/rules/01-design-system.mdc`

## 実行手順
1. **目的整理**: 何を改善するか（LCP/CLS/INP/アクセシビリティ/SEO）
2. **診断**: Lighthouse/DevTools で現状を計測
3. **原因特定**: 主要ボトルネック（画像/JS/フォント/レイアウト）
4. **改善設計**: 影響の大きい順に対策案を作る
5. **検証**: 再計測して効果を確認

## チェックリスト
- 画像/フォントの最適化をしている
- CLS対策（サイズ確保、遅延コンテンツの安定化）
- 入力遅延（INP）対策の優先順位が明確
- アクセシビリティ（コントラスト、フォーカス、見出し構造）

## 出力テンプレ
1. 改善目標
2. 計測結果（Before/After）
3. 実施した対策
4. 残課題
