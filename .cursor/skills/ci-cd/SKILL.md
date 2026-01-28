---
name: ci-cd
description: CI/CDパイプライン設計・最適化・セキュリティ導入の手順。GitHub Actions/GitLab CIでの運用時に使用。
license: MIT
metadata:
  author: ahmedasmar
  source: https://github.com/ahmedasmar/devops-claude-skills
---

# CI/CD Pipelines

CI/CDを安全かつ高速に回すための実行手順です。

## いつ使うか

- 新規パイプライン設計
- CIが遅い/不安定/失敗が多い
- セキュリティスキャンを組み込みたい

## 実行手順

1. **対象整理**: 対象リポジトリ、言語、ビルド方式を確認する。
2. **基本構成を決める**:
   - lint → unit → integration → build → deploy
3. **速度最適化**:
   - 依存キャッシュ
   - 並列実行（matrix）
   - パスフィルタで不要な実行を削減
4. **安全性強化**:
   - OIDCでクラウド認証
   - 最小権限とシークレット管理
   - SAST/DAST/SCA/シークレットスキャンを導入
5. **信頼性強化**:
   - タイムアウト設定
   - フレーク対策（再実行/安定化）
6. **デプロイ設計**:
   - 本番は承認ゲートやヘルスチェックを用意
7. **改善ループ**:
   - 失敗原因の分類
   - 実行時間の継続監視

## 参照

- https://github.com/ahmedasmar/devops-claude-skills
