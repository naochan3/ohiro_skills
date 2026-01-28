---
name: deployment-paas
description: Vercel/RailwayなどPaaSへのデプロイ手順。
---
# Deployment (PaaS)

## When to Use
- Vercel / Railway などにデプロイする時

## Instructions
1. **環境変数の整理と登録**
   - 本番用の `.env` から必要項目を洗い出し、ダッシュボードに登録
2. **プラットフォーム固有の設定**
   - `vercel.json` / `railway.json` などが必要か確認して追加
3. **デプロイ実行**
   - 既存のCI/CDがある場合はその手順に従う
4. **ログ確認とトラブルシュート**
   - ビルドログ / ランタイムログを確認し、失敗箇所を特定
5. **サーバーレス特性の考慮**
   - タイムアウト、ステートレス、コールドスタートを前提に設計

## References
- `@/.cursor/rules/13-deployment-paas.mdc`
