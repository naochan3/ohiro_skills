---
name: varlock
description: 環境変数/シークレットを安全に扱う手順。APIキーや認証情報を扱うときに使用。
license: MIT
metadata:
  author: dmno-dev
  source: https://github.com/wrsmith108/varlock-claude-skill
  docs: https://varlock.dev
---

# Varlock

シークレットを**表示しない**運用のための手順です。

## いつ使うか

- APIキー/DB接続文字列/認証情報を扱うとき
- `.env` / `secrets` / `credentials` が話題に出たとき

## 実行手順

1. **絶対に表示しない**:
   - `.env` を読み込まない
   - `echo $SECRET` や `printenv` を使わない
2. **スキーマを使う**:
   - 値ではなく `.env.schema` を参照して定義を管理
3. **検証はVarlock**:
   - `varlock load` で存在/形式を検証（値はマスク）
4. **実行はVarlock経由**:
   - `varlock run -- <command>` で安全に実行
5. **漏洩対応**:
   - 露出が疑われたら即時ローテーション

## 参照

- https://github.com/wrsmith108/varlock-claude-skill
- https://varlock.dev
