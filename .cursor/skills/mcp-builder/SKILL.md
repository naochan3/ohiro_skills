---
name: mcp-builder
description: MCPサーバーを設計・実装・検証するための手順。外部API連携やツール公開時に使用。
license: Apache-2.0
metadata:
  author: Anthropic
  source: https://github.com/anthropics/skills
---

# MCP Builder

MCPサーバーを高品質に作るための実行手順です。

## いつ使うか

- 外部API連携をMCP化したい
- 新規ツールを追加/設計したい
- MCPサーバーの品質を上げたい

## 実行手順

1. **設計**:
   - エンドポイントとユースケースを洗い出す
   - ツール名は動詞ベースで統一
2. **スキーマ設計**:
   - 入力/出力の型と制約を明確化
   - 返すデータは最小化し、ページングを意識
3. **実装**:
   - エラーメッセージは行動可能な形で返す
   - readOnly/destructive/idempotent のヒントを明記
4. **検証**:
   - 主要ユースケースで動作確認
   - 境界条件（空/大量/権限不足）を検証
5. **評価**:
   - 実タスクに近い質問で精度検証
   - 不足ツールやデータ欠落を補強

## 参照

- https://github.com/anthropics/skills
