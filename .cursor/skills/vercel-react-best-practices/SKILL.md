---
name: vercel-react-best-practices
description: React/Next.jsの性能最適化の実践手順。コンポーネント、データ取得、バンドル最適化、再レンダリング調整時に使用。
license: MIT
metadata:
  author: Vercel
  source: https://github.com/vercel-labs/agent-skills
  version: "1.0.0"
---

# Vercel React Best Practices

VercelがまとめたReact/Next.jsの性能ガイドを、日本語の実行手順として整理したスキルです。

## いつ使うか

- 新規のReact/Next.js実装
- パフォーマンス改善（LCP/TTFB/JS実行/バンドル）
- 大きなリファクタリングや構成見直し

## 実行手順

1. **目的の明確化**: 改善対象を決める（例: TTFB/LCP/バンドルサイズ/JS実行/再レンダリング）。
2. **ウォーターフォール排除**:
   - 独立処理は `Promise.all` で並列化
   - awaitは必要な分岐内に移動
   - `Suspense` でストリーミングを活用
3. **バンドル最適化**:
   - バレルインポートを避ける
   - 重いUIは `next/dynamic` で分割
   - サードパーティはハイドレーション後に読み込み
4. **サーバー側最適化**:
   - データ取得の重複を避ける（キャッシュ/デデュープ）
   - クライアントに渡すデータを最小化
   - 直列フェッチを並列化
5. **クライアント側最適化**:
   - SWR/React Query等で重複リクエストを抑制
   - グローバルイベントを重複登録しない
6. **再レンダリング最適化**:
   - `useMemo`/`memo` は重い計算のみ
   - `useTransition` で非緊急更新を分離
   - 依存配列はプリミティブ中心に整理
7. **レンダリング負荷の抑制**:
   - 長いリストは `content-visibility` を検討
   - 静的JSXはコンポーネント外へホイスト
8. **検証**: Lighthouse/React Profiler/DevToolsで効果確認。

## 参照

- https://github.com/vercel-labs/agent-skills
