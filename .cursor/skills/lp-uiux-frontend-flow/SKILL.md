---
name: lp-uiux-frontend-flow
description: LP制作・UI/UX・フロントエンド実装の作業フローと品質基準を定義する。LP作成、ランディングページ、UI/UX、画面設計、フロント実装の依頼時に使用。
---
# LP / UIUX / Frontend Flow

## いつ使うか
- 「LPを作成して」「ランディングページ作成」などの依頼
- UI/UX設計やフロントエンド実装の依頼

## 優先するルール
- `.cursor/rules/01-design-system.mdc`
- `.cursor/rules/26-implementation-process.mdc`
- `.cursor/rules/45-image-generation-flow.mdc`

## コア原則
- 絵文字アイコンは使用禁止。アイコンはLucide/HeroiconsなどのSVGを使う
- 主要CTAを1つ定め、導線（視線とクリックの流れ）を設計する
- 情報設計→レイアウト→実装の順で進める

## 作業フロー
1. 目的・対象ユーザー・主要CTAを整理する
2. セクション構成（IA）を作成する
3. トーン/配色/タイポグラフィ方針を決める
4. コンポーネント構成と責務分割を決める
5. 実装し、レスポンシブとa11yを確認する
6. 画像が無ければ生成→`public/images` に配置→UIに反映する

## LP構成の基本テンプレ
- Hero（価値提案 + CTA）
- Features（3〜6個）
- Proof（実績/レビュー/数値）
- Use cases / Flow（利用の流れ）
- FAQ / CTA（最後の意思決定支援）

## Figmaがある場合
- `figma-implement-design` の手順を優先する
