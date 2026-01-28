---
name: threejs-react-workflow
description: three.jsとReact Three Fiberの導入から最適化までを整理する。
---
# Three.js React Workflow

## いつ使うか
- 3D表現をWebに組み込みたい時
- React + 3Dの構成を選定する時

## 参照ルール（最優先）
- `.cursor/rules/25-performance-tuning.mdc`

## 要点
- three.js基礎（Scene/Camera/Renderer）を理解する
- R3Fでコンポーネント化し、dreiでヘルパーを使う
- Next.js利用時はテンプレートで統合する

## 手順
1. 3D表現の目的と負荷を定義
2. three.js基礎構成を決める
3. R3Fでコンポーネント化
4. dreiでカメラ/コントロール/ローダーを追加
5. Next.js統合（必要時）

## チェックリスト
- 描画負荷の上限が決まっている
- モデル/テクスチャの最適化方針がある
- レンダリング更新が最小化されている

## 出力テンプレ
1. 目的/表現
2. 技術選定（三者の役割）
3. コンポーネント構成
4. 最適化方針
