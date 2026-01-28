---
name: vercel-react-native-skills
description: React Native/Expoの性能・UX最適化の手順。モバイルアプリ、リスト、アニメーション、画像最適化時に使用。
license: MIT
metadata:
  author: Vercel
  source: https://github.com/vercel-labs/agent-skills
  version: "1.0.0"
---

# Vercel React Native Skills

React Native/Expoの実装で起きがちな性能問題を避けるための手順です。

## いつ使うか

- React Native/Expoアプリの実装
- リストが重い/スクロールがカクつく
- アニメーションや画像最適化を行う

## 実行手順

1. **リスト性能**:
   - 大規模リストは `FlashList` を優先
   - アイテムコンポーネントは `memo` 化
   - インライン関数/スタイルを避ける
2. **アニメーション**:
   - `transform` と `opacity` を基本にする
   - `useDerivedValue` を使い計算を分離
3. **ナビゲーション**:
   - 可能ならネイティブスタック/タブを使う
4. **UI/画像**:
   - 画像は `expo-image` 等の最適化を利用
   - セーフエリアを必ず考慮
5. **状態管理**:
   - 状態の購読を最小化
   - 非同期更新は一括化
6. **構成**:
   - モノレポは依存関係の重複を避ける
   - ネイティブ依存はアプリ側に集約

## 参照

- https://github.com/vercel-labs/agent-skills
