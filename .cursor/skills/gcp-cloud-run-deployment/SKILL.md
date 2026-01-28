---
name: gcp-cloud-run-deployment
description: Cloud Runへのデプロイを自動化・標準化する手順。
---
# GCP Cloud Run Deployment

## When to Use
- GCP Cloud Run へデプロイする時

## Instructions
1. **必要な成果物の準備**
   - Dockerfile / GitHub Actions / 環境変数 を揃える
2. **Cloud SQL連携の設計**
   - 接続方式、シークレット管理、接続テストを整理
3. **ヘルスチェックの実装**
   - `/health` エンドポイントを追加
4. **自動化スクリプトの活用**
   - 既存の自動化スクリプトを必要に応じて実行

## References
- `@/.cursor/rules/20-gcp-deploy-complete-guide.mdc`
