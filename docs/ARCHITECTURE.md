# ARCHITECTURE.md - システム設計・技術選定

## 1. 技術スタック
- **Frontend Framework**: React (TypeScript)
- **Build Tool / Bundler**: Vite
- **Styling**: Tailwind CSS
- **Testing Framework**: Playwright (TypeScript)

## 2. 技術選定理由 (ADR)
- **Vite**: 開発サーバーの超高速起動とプロダクションビルドの最適化。
- **Tailwind CSS**: ユーティリティクラスによる迅速な開発と、ダークモード（`dark:`）およびアニメーションクラスの標準化。
- **Playwright**: TypeScript による型安全で信頼性の高いE2E/UI自動テスト環境。

## 3. モジュール構成方針
- `src/components/`: 単一責任の再利用可能なUIコンポーネント。
- `src/hooks/`: テーマ切り替えや状態管理のカスタムフック。
- `tests/`: 機能ごとの Playwright E2E テストシナリオファイル（`.spec.ts`）。



追記

## 1. データ永続化方針 (Data Persistence)
- **保存基盤**: ブラウザ標準の `localStorage` を使用する。
- **外部依存の排除**: サーバーサイドDBや外部APIへの保存処理は導入せず、完全クライアントサイドで完結させる。
