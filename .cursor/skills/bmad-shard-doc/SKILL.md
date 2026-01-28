---
name: bmad-shard-doc
description: 大きなMarkdownを見出し単位で分割し、索引を生成する手順。
---
# BMAD: Shard Document

## When to Use
- 大きなMarkdownをセクション単位で分割したいとき
- セクションごとの編集/管理が必要なとき

## Instructions
1. **元ファイルの確認**
   - 対象のMarkdownパスを確認する
   - `.md` であることを検証する
2. **出力先の決定**
   - 既定: 元ファイルと同階層に「元ファイル名/」を作成
   - 例: `/path/to/architecture.md` → `/path/to/architecture/`
3. **分割実行**
   - `npx @kayvan/markdown-tree-parser explode [source] [dest]`
4. **出力確認**
   - 分割ファイルと `index.md` が生成されたか確認する
5. **完了報告**
   - 元ファイル/出力先/作成数/注意点を報告する
6. **元ファイルの扱い**
   - 推奨は削除 or アーカイブ
   - 保持する場合は重複のリスクを警告する

## References
- `_bmad/core/tasks/shard-doc.xml`
