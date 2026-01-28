---
name: skill-creator
description: 新規スキルを定義・構成・検証するための手順。SKILL.md作成時に使用。
license: Apache-2.0
metadata:
  author: Anthropic
  source: https://github.com/anthropics/skills
---

# Skill Creator

スキルを「定義 → 設計 → 検証」するための手順です。

## いつ使うか

- 新規スキルを作るとき
- 既存スキルを標準形式に整理するとき

## 実行手順

1. **目的とトリガー**:
   - 何を解決するスキルかを1文で定義
   - どの依頼文で発動するかを列挙
2. **スキル名と説明**:
   - `name` は小文字・ハイフンで一意にする
   - `description` に「いつ使うか」を明記
3. **自動/手動の方針**:
   - 自動適用が不要なら `disable-model-invocation: true`
4. **構成**:
   - `SKILL.md` を中心に、必要なら `references/` や `scripts/` を追加
5. **指示内容**:
   - 具体的な手順を番号で記述
   - 禁止事項や注意点を明確化
6. **検証**:
   - 典型的な依頼文で動作を確認
   - 誤発動や冗長さを調整

## 参照

- https://github.com/anthropics/skills
