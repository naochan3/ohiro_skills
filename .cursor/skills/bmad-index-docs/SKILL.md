---
name: bmad-index-docs
description: 指定ディレクトリのドキュメントを走査し、index.md を生成/更新する手順。
---
# BMAD: Index Docs

## When to Use
- ドキュメントが増えて把握しづらくなったとき
- `index.md` を自動生成/更新したいとき

## Instructions
1. **対象ディレクトリを決める**
   - 対象が未指定ならパスを確認する
2. **一覧の取得**
   - 対象配下のファイル/サブディレクトリを列挙する
3. **グルーピング**
   - 種類/用途/サブディレクトリで分類する
4. **内容確認と要約**
   - 各ファイルを読み、内容に基づいて3〜10語で説明文を作る
5. **index.md を作成/更新**
   - 相対パス（`./`）でリンクを貼る
   - グループ内はアルファベット順に並べる
6. **検証**
   - 書き込み権限がない場合は中断する
   - 隠しファイルは基本スキップ（明示指定があれば含める）

## Output Format（例）
```md
# Directory Index

## Files

- **[filename.ext](./filename.ext)** - Brief description

## Subdirectories

### subfolder/

- **[file1.ext](./subfolder/file1.ext)** - Brief description
```

## References
- `_bmad/core/tasks/index-docs.xml`
