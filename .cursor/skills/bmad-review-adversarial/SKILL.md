---
name: bmad-review-adversarial
description: 仕様・差分・ドキュメントを懐疑的にレビューし、最低10件の指摘を列挙する手順。
---
# BMAD: Adversarial Review (General)

## When to Use
- 仕様/差分/ドキュメントの抜け漏れを強く洗い出したいとき
- 「問題がある前提」で検証したいとき

## Instructions
1. **対象の確認**
   - 何をレビューするかを明確にする（diff/spec/doc など）
2. **徹底的に疑う**
   - 不備がある前提で見つける
3. **最低10件の指摘**
   - 量がゼロなら再分析
4. **出力**
   - Markdownの箇条書き

## References
- `_bmad/core/tasks/review-adversarial-general.xml`
