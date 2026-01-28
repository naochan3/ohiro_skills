---
name: rule-bootstrap
description: 新規プロジェクトや大規模機能追加時のルール環境構築手順。
---
# Rule Bootstrap
プロジェクト開始時に「ルール環境を整えてから作業に入る」ための手順です。

## When to Use
- 新規プロジェクトの作成時
- 大規模機能追加でルールの再整理が必要な時

## Instructions
1. **プロジェクトタイプを判定**
   - Frontend / Backend / Fullstack / Infra / AI-CLI を分類
2. **プロジェクト土台作成**
   - PowerShell で `mkdir [project-name]; cd [project-name]`
3. **ルールの選定とコピー**
   - `.cursor/rules/00-rule-selector.mdc` の選定ロジックに従う
   - `.cursor/rules/` を作成し、必要な `.mdc` を配置
4. **固有ルールの追加**
   - `.cursor/rules/99-project-specific.mdc` を作成し、差分要件を明記
5. **使用ルールの記録**
   - 可能なら `RULES_USED.md` を更新

## Optional Script
- `@/.cursor/rules/scripts/copy-rules-to-project.ps1`

## References
- `@/.cursor/rules/00-rule-selector.mdc`
- `@/.cursor/rules/00-index.mdc`
