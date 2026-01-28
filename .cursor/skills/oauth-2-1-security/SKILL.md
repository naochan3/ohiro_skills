---
name: oauth-2-1-security
description: OAuth 2.1の必須要件（PKCE、リダイレクト検証、トークン運用）を整理する。
---
# OAuth 2.1 Security

## いつ使うか
- OAuthを導入する時
- 認可フローの設計/レビュー時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`

## 要点
- PKCEは必須（S256推奨）
- リダイレクトURIは完全一致で検証
- Bearerトークンはヘッダーで送信
- インプリシット/パスワードフローは使わない

## チェックリスト
- PKCE（code_challenge/code_verifier）を実装している
- リダイレクトURIが登録済み完全一致
- 認可コードはワンタイム
- アクセストークンは短命
- スコープは最小権限
- TLS必須

## 出力テンプレ
1. 採用フロー
2. PKCE設定
3. トークン運用方針
4. 例外/制限事項
