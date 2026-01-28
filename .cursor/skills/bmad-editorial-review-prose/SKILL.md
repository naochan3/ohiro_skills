---
name: bmad-editorial-review-prose
description: 文章の可読性と明確さを損なう表現を最小限の修正で指摘・改善する校正手順。
---
# BMAD: Editorial Review - Prose

## When to Use
- 文章の表現が分かりにくい/誤解される可能性があるとき
- 文体は保ちつつ、明確さだけを改善したいとき

## Instructions
1. **入力検証**
   - 3語未満は中断
   - `reader_type` は `humans` / `llm` のみ
2. **文体の把握**
   - 既存のトーン/語彙/技術用語を維持する
3. **問題点の抽出**
   - 意味が不明確/誤解されやすい表現のみ対象
   - コード/フロントマター/構造マークアップは除外
4. **最小修正**
   - 内容を変えず、表現だけを明確化
5. **出力**
   - 3列テーブル（Original / Revised / Changes）
   - 問題なしなら「No editorial issues identified」

## Output Format（例）
| Original Text | Revised Text | Changes |
|---|---|---|
| The system will processes data and it handles errors. | The system processes data and handles errors. | 主語と動詞の一致、冗長表現の削除 |

## References
- `_bmad/core/tasks/editorial-review-prose.xml`
