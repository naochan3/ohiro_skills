---
name: docker-best-practices
description: Dockerfileを安全かつ軽量に作るための実践手順。
---
# Docker Best Practices

## When to Use
- Dockerfileの新規作成や見直しを行うとき

## Instructions
1. **ベースイメージの固定**
   - `node:20-alpine` など、メジャー固定の軽量イメージを選ぶ
2. **`.dockerignore` を作成**
   - `node_modules`, `.git`, `dist`, `coverage`, `.env` などを除外
3. **マルチステージビルド**
   - ビルド用と実行用を分離し、成果物のみコピー
4. **非rootユーザーで実行**
   - `adduser` で専用ユーザーを作成し `USER` を切り替え
5. **ヘルスチェックの追加**
   - `/health` を叩く `HEALTHCHECK` を設定
6. **脆弱性スキャン**
   - Trivy などで定期スキャンを行う

## References
- `@/.cursor/rules/12-docker-best-practices.mdc`
