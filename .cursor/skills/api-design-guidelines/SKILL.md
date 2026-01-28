---
name: api-design-guidelines
description: REST APIの設計基準（命名、HTTP、互換性、エラー形式）を統一する。
---
# API Design Guidelines

## いつ使うか
- 新規API設計や既存APIの再設計
- 命名/レスポンス/バージョニングの統一が必要な時

## 参照ルール（最優先）
- `.cursor/rules/09-integration-and-api-contracts.mdc`
- `.cursor/rules/23-security-policy.mdc`

## 要点（統合）
- リソース指向でURLを設計する
- HTTPメソッドとステータスコードを厳密に使い分ける
- エラーフォーマットを統一する
- 互換性とバージョニングを計画する

## チェックリスト
- URLは名詞の複数形で設計されている
- メソッドは責務に一致している（GET/POST/PUT/PATCH/DELETE）
- ステータスコードが意味通りに使われている
- エラーレスポンス形式が統一されている
- ページネーション方針が明記されている
- バージョニング方針が決まっている

## 出力テンプレ
1. リソース一覧とURL設計
2. メソッド/ステータスの対応表
3. エラーレスポンス形式
4. バージョニング/互換性方針
