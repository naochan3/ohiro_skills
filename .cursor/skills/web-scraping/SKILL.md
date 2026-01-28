---
name: web-scraping
description: 倫理的かつ堅牢なWebスクレイピングの実装手順。
---
# Web Scraping

## When to Use
- Webスクレイピング機能を設計・実装する時

## Instructions
1. **倫理・規約の確認**
   - `robots.txt` の確認、利用規約に違反しない範囲で行う
2. **アクセス制御**
   - `User-Agent` を明示し、リクエスト間隔を設定する
3. **ツール選定**
   - 静的: `fetch` / `axios` / `requests`
   - 動的: Playwright / Puppeteer
4. **堅牢な抽出**
   - セレクタは安定した属性を優先、失敗時のフォールバックを用意
5. **データ品質の担保**
   - `zod` などでスキーマ検証し、欠損時の扱いを決める
6. **キャッシュと再取得**
   - 再取得頻度とキャッシュポリシーを定義する

## References
- `@/.cursor/rules/14-scraping-rules.mdc`
