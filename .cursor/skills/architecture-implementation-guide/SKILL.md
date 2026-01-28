---
name: architecture-implementation-guide
description: Clean Architecture/DDD/Hexagonalの選択と実装手順を統合する。
---
# Architecture Implementation Guide

## いつ使うか
- 新規アプリのアーキテクチャ選定時
- ドメイン中心設計に移行したい時
- CQRS/ユースケース分離を導入したい時

## 参照ルール（最優先）
- `.cursor/rules/40-architecture-and-layering.mdc`
- `.cursor/rules/26-implementation-process.mdc`

## 要点（統合）
- Clean Architectureは依存方向と境界の設計が核心
- DDDはユビキタス言語と境界づけられたコンテキストが起点
- Hexagonalは入出力ポートの明示化でテスタブルにする

## 手順
1. ドメイン境界とユースケースを定義
2. レイヤー構成（Domain/Application/Infrastructure/UI）を確定
3. ポート/アダプタを設計し依存方向を固定
4. コマンド/クエリの責務を分離
5. ドメインイベントの発火点を設計

## チェックリスト
- 依存方向が内側に向いている
- ドメイン層がフレームワーク依存でない
- ユースケース単位でテスト可能
- 外部I/Oがアダプタに閉じている

## 出力テンプレ
1. 境界づけられたコンテキスト
2. レイヤー構成と依存方向
3. ポート/アダプタ一覧
4. コマンド/クエリ分離方針
