---
name: bmad-editorial-review-structure
description: 文書構成の冗長・重複・順序を指摘し、構造改善の提案を行う手順。
---
# BMAD: Editorial Review - Structure

## When to Use
- 文書が長く、構成が分かりにくいとき
- 章立てや順序の改善案が欲しいとき

## Instructions
1. **入力検証**
   - 3語未満は中断
   - `reader_type` は `humans` / `llm` のみ
2. **目的と読者の把握**
   - `purpose` / `target_audience` があれば優先
   - なければ内容から推定する
3. **構造モデルの選定**
   - チュートリアル/リファレンス/概念説明/戦略文書など
4. **構造レビュー**
   - CUT / MERGE / MOVE / CONDENSE / QUESTION / PRESERVE で分類
5. **出力**
   - 要約 → 推奨一覧 → 削減見積もり
   - 問題なしなら「No substantive changes recommended」

## Output Format（例）
```
## Document Summary
- **Purpose:** ...
- **Audience:** ...
- **Reader type:** ...
- **Structure model:** ...
- **Current length:** ...

## Recommendations
### 1. CUT - [Section]
**Rationale:** ...
**Impact:** ...
```

## References
- `_bmad/core/tasks/editorial-review-structure.xml`
