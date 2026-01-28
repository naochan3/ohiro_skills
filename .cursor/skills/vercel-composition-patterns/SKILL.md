---
name: vercel-composition-patterns
description: Reactのコンポジション設計を見直すための手順。Boolean propsの増殖や再利用性の低下が見えた時に使用。
license: MIT
metadata:
  author: Vercel
  source: https://github.com/vercel-labs/agent-skills
  version: "1.0.0"
---

# Vercel Composition Patterns

拡張性の高いReactコンポーネント設計に向けた手順を整理したスキルです。

## いつ使うか

- boolean props が増えすぎたコンポーネント
- 再利用しづらいコンポーネント設計
- 複雑なUIをコンポーネントライブラリ化したい時

## 実行手順

1. **問題抽出**: boolean propsや条件分岐の乱立箇所を特定する。
2. **コンポジション優先**:
   - `children` で構成できる形に寄せる
   - 可能なら「明示的なバリアント部品」を用意
3. **Compound Components**:
   - 親がContextで共有状態を持つ構成に整理
   - 子コンポーネントは役割ごとに分割
4. **状態の持ち方を整理**:
   - Providerが状態の出どころを一元化
   - 状態・操作・メタ情報のインターフェースを定義
5. **APIの単純化**:
   - 余計なプロップの削減
   - 外部に公開するAPIを最小限に保つ

## 参照

- https://github.com/vercel-labs/agent-skills
