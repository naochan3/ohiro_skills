---
name: supabase-postgres-best-practices
description: Supabase/Postgresの性能・安全性のベストプラクティスを適用するための実行手順。SQLやスキーマ、接続管理、RLSを扱うときに使用。
license: MIT
metadata:
  author: Supabase
  source: https://github.com/supabase/agent-skills
  version: "1.1.0"
  date: "2026-01"
---

# Supabase Postgres Best Practices

SupabaseがまとめたPostgres最適化の要点を、実装で使える手順に整理したスキルです。

## いつ使うか

- SQLクエリを新規作成/レビュー/最適化するとき
- スキーマやインデックス設計を決めるとき
- 接続数、プール、タイムアウトを調整するとき
- RLSや権限設計を見直すとき
- 速度やロック競合、スケールで詰まったとき

## 実行手順

1. **前提整理**: ワークロード (読み/書き比率、主要な検索条件、許容レイテンシ) を整理する。
2. **現状診断**: `EXPLAIN (ANALYZE, BUFFERS)` と `pg_stat_statements` でボトルネックを特定する。
3. **クエリ最適化**:
   - 不要な `SELECT *` を避け、必要列のみ取得
   - N+1を避けるためにJOIN/バッチ取得を検討
   - 条件列の索引と並びを見直す
4. **スキーマ/インデックス設計**:
   - 適切な型、主キー/外部キー/複合索引/部分索引を設計
   - `jsonb` は用途に応じてGIN/GiSTを使い分け
5. **接続管理**:
   - コネクションプールを前提に設計
   - 上限値、アイドルタイムアウト、プリペアドステートメントを調整
6. **同時実行/ロック対策**:
   - トランザクションは短く
   - `SKIP LOCKED` やアドバイザリロックを必要に応じて採用
7. **セキュリティ/RLS**:
   - RLSを有効化し、最小権限でポリシーを設計
   - サービスロールキーはサーバー側のみで使用
8. **監視/運用**:
   - `VACUUM`/`ANALYZE` の状況を監視
   - 遅いクエリ、ロック待ちを定期観測

## 呼び出し

- 自動適用: SQL/スキーマ/性能/接続/ RLS が話題に上がった場合
- 手動: `/supabase-postgres-best-practices`

## 参照

- Supabase Agent Skills: https://github.com/supabase/agent-skills
- Postgres Docs: https://www.postgresql.org/docs/current/
- Supabase Docs: https://supabase.com/docs
- RLS: https://supabase.com/docs/guides/auth/row-level-security
