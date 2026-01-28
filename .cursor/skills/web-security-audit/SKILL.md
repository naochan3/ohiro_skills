---
name: web-security-audit
description: OWASP Top 10と主要チートシートに基づき、Webセキュリティ監査項目を整理する。
---
# Web Security Audit

## いつ使うか
- セキュリティレビュー/監査
- 新規機能の脅威評価

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`

## 主要チェック（OWASP Top 10）
- 認可制御の不備
- 暗号化の失敗
- インジェクション
- 不安全な設計
- セキュリティ設定ミス
- 脆弱なコンポーネント
- 認証の失敗
- ソフトウェア/データ整合性の失敗
- ログ/監視の不備
- SSRF

## HTML5周辺チェック
- `postMessage`のorigin検証
- CORSは許可リスト方式
- Local Storageに機密情報を保存しない
- 外部リンクに`rel="noopener noreferrer"`
- iframeに`sandbox`を適用

## 出力テンプレ
1. 対象範囲
2. OWASP Top 10の該当項目
3. HTML5特有の注意点
4. 対策/残リスク
