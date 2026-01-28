---
name: static-to-dynamic
description: 静的UIを動的アプリへ変換する段階的手順。
---
# Static to Dynamic

## When to Use
- 静的HTML/CSSを動的アプリへ移行する時

## Instructions
1. **構造の解析とコンポーネント化計画**
   - UIを責務ごとに分割し、再利用単位を決める
2. **コンポーネントの実装**
   - プレゼンテーションと状態管理を分離する
3. **データ契約の定義**
   - 必要なAPI/型を先に定義する
4. **バックエンドAPIの実装**
   - 契約に従って実装・検証する
5. **フロントとの接続**
   - ローディング/エラー/成功の状態管理を追加する

## References
- `@/.cursor/rules/17-static-to-dynamic-workflow.mdc`
