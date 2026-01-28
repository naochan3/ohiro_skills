---
name: iframe-resizer-integration
description: iframe-resizerを安全に導入し、iframeサイズ同期を行う手順。
metadata:
  author: David J. Bradshaw
  source: https://github.com/davidjbradshaw/iframe-resizer
  license_note: GPLv3または商用ライセンスのデュアルライセンス
---
# iframe-resizer Integration
## いつ使うか
- iframeの高さが可変でレイアウト崩れが起きる時
- クロスドメインiframeのサイズ同期が必要な時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`

## 実行手順
1. **ライセンス確認**: GPLv3または商用ライセンスの適用範囲を確認する
2. **親/子の役割分担**: 親ページとiframe内のスクリプト配置を決める
3. **許可ドメイン設計**: クロスドメイン連携時の許可範囲を定義する
4. **イベント設計**: リサイズ/スクロール/メッセージのイベントを整理する
5. **監視と検証**: 主要ページでリサイズの安定性を確認する

## 注意点
- 具体コードの転載は行わず公式ドキュメントを参照する
- 取り扱う情報は最小限にし、iframe間通信の範囲を限定する

## チェックリスト
- ライセンス条件を満たしている
- 許可ドメインが限定されている
- エラー時にレイアウトが破綻しない

## 出力テンプレ
1. 対象iframe
2. 親/子の配置方針
3. 許可ドメイン
4. 検証結果
