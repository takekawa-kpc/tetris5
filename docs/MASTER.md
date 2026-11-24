# MASTER.md - プロジェクトインデックス & 共通ルール

## 1. プロジェクト概要
- **プロジェクト名**: [プロジェクト名]
- **目的**: React/Vite/Tailwind CSS によるモダン＆ミニマルな Web アプリケーション開発
- **主要技術スタック**: React, Vite, Tailwind CSS, TypeScript, Playwright

## 2. コミュニケーション & AI協働ルール
- **対話言語**: 日本語で対話すること。
- **AIエージェント対応方針**:
  - コード解説は最小限にし、すぐ動かせる実行コマンドや修正済みコードの提示を優先すること。
  - 余計な前置きや長文解説を避け、コピー＆ペーストしてそのまま使えるコードブロックを先頭に提示する。

## 3. コア7文書索引
| 文書名 | 役割 | 扱う情報 | 更新日 |
| :--- | :--- | :--- | :--- |
| [PROJECT.md](./PROJECT.md) | ビジョンと要件 | 目的、デザインビジョン、主要機能、非機能要件 | YYYY-MM-DD |
| [ARCHITECTURE.md](./ARCHITECTURE.md) | システム設計 | 技術スタック、ディレクトリ構造、技術選定理由（ADR） | YYYY-MM-DD |
| [DOMAIN.md](./DOMAIN.md) | ビジネスロジック | テーマ管理ルール、UI状態遷移・発火条件 | YYYY-MM-DD |
| [PATTERNS.md](./PATTERNS.md) | 実装パターン | AI出力規約、Tailwind CSS/UI実装パターン | YYYY-MM-DD |
| [TESTING.md](./TESTING.md) | テスト戦略 | Playwright + TypeScript によるテスト規約・実行コマンド | YYYY-MM-DD |
| [DEPLOYMENT.md](./DEPLOYMENT.md) | 運用・リリース | Vite ビルド手順、CI/CD、リリース前品質ゲート | YYYY-MM-DD |

## 4. ディレクトリ構造
```text
.
├── AGENTS.md            # Layer 1: 薄いエントリーポイント（自動読み込み設定）
├── .github/             # GitHub 設定・テンプレート
│   └── ISSUE_TEMPLATE/ # Issue テンプレート（タスク作成用）
├── docs/                # Layer 2: コア7文書
│   ├── MASTER.md
│   ├── PROJECT.md
│   ├── ARCHITECTURE.md
│   ├── DOMAIN.md
│   ├── PATTERNS.md
│   ├── TESTING.md
│   └── DEPLOYMENT.md
├── src/                 # アプリケーションソースコード
│   ├── components/
│   ├── hooks/
│   └── styles/
└── tests/               # Playwright（TypeScript）テストコード
5. 最重要制約
デザインは「モダンでミニマル」「ダークモード対応」「美しいアニメーション」を必須とする。
テストコードは Playwright を使用し、すべて TypeScript で作成すること。



追記

## 1. プロジェクト概要
- **プロジェクト名**: PC Web テトリス
- **概要**: `localStorage` を活用したPCブラウザ専用のテトリスアプリケーション
