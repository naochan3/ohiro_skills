---
name: requirements-definition
description: 要件が曖昧なときに、ビジョンから受け入れ条件までを整理する手順。
---
# Requirements Definition
要件が曖昧な場合に「なぜ作るか → 誰が使うか → 何を満たすか」を段階的に固めます。

## When to Use
- 依頼が抽象的で実装開始が危険なとき
- 目的、対象ユーザー、成功指標が曖昧なとき
- 画面や機能の範囲が未定義なとき

## Instructions
1. **ビジョン定義**（課題/ターゲット/解決策の核）
   - `docs/vision.md` に Problem / Target / Core Solution を書く
   - KPI（定量）と定性ゴールを併記する
2. **利用文脈の仮説**（Trigger/Goal/Pain）
   - 利用場面を最低5つ列挙する
   - 入口→ゴールまでの体験を短文でまとめる
3. **ユーザーストーリー**
   - `docs/requirements.md` に 3C（As a / I want / So that）で記述
4. **受け入れ条件**
   - Given/When/Then で正常系・異常系を明確化
5. **画面遷移と情報設計**
   - `docs/ux/sitemap.md` に `stateDiagram` を作成
   - Z/Fパターン、グルーピング、プログレッシブ開示を整理
6. **用語集とドメインモデル**
   - `docs/domain/glossary.md` に用語集（日本語/英語/定義/NG）を作成
   - `docs/domain/model.md` に Entity / Value Object を整理
   - 必要なら `classDiagram` を追加
7. **複雑フローはシーケンス図で補足**
   - `docs/usecases/` 配下に `sequenceDiagram` を作成
8. **最後に整合確認**
   - `26-implementation-process.mdc` の Phase 1 と整合しているか確認
   - 前提は「仮定」として明示し、後で更新できる形にする

## References
- `@/.cursor/rules/31-product-vision-and-problem-framing.mdc`
- `@/.cursor/rules/32-functional-requirements-and-usecases.mdc`
- `@/.cursor/rules/33-domain-modeling-and-glossary.mdc`
- `@/.cursor/rules/37-ux-research-and-ia.mdc`
- `@/.cursor/rules/26-implementation-process.mdc`
