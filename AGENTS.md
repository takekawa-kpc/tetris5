# AGENTS.md - AI Agent Entrypoint

## 1. エントリーポイント指示 (MUST READ FIRST)
- 作業を開始する前に、必ず **`docs/MASTER.md`** を読み込み、プロジェクト全体の仕様構造および参照すべき仕様書を把握してください。
- 事実、合意済みの決定事項、および未決定事項を明確に区別して扱ってください。

## 2. AI基本行動規約
- **対話言語**: すべてのやり取りは**日本語**で行ってください。
- **コード出力方針**:
  - コード解説は必要最小限にとどめてください。
  - すぐに実行・試行できるコマンド（例: `npm run dev`, `npx playwright test`）や、コピー＆ペーストでそのまま置き換え可能な完全なコードブロックを最優先で提示してください。
- **手編集の尊重**: ユーザーの手編集箇所や既存のルールを無条件で上書き・削除しないでください。

## 3. 標準 Git Workflow
タスク指示（Issue 等）を受けた場合、以下の手順に従って自律的に進めてください：

1. **仕様と条件の確認**: 対象 Issue を確認し、受け入れ基準および `docs/` 配下の関連仕様書を読み込む。
2. **ブランチ作成**: `feature/#<Issue番号>-<タスクの簡潔な英語説明>` 形式で作業ブランチを作成。
3. **実装 & テスト**:
   - `docs/PATTERNS.md` および `docs/ARCHITECTURE.md` に従って実装。
   - `docs/TESTING.md` に従い、Playwright (TypeScript) でテストを作成・実行してパスさせる。
4. **コミット**: Conventional Commits 形式（例: `feat: ...`, `fix: ...`）で細かくコミット。
5. **PR作成**: 作業完了後、`develop` または `main` ブランチへ向けた Pull Request を作成する。

## 4. プロジェクト参照マップ
- **マスターインデックス**: `docs/MASTER.md`
- **デザイン・要件**: `docs/PROJECT.md`
- **技術選定・構造**: `docs/ARCHITECTURE.md`
- **ドメインロジック**: `docs/DOMAIN.md`
- **コーディング規約**: `docs/PATTERNS.md`
- **テスト規約**: `docs/TESTING.md`
- **ビルド・デプロイ**: `docs/DEPLOYMENT.md`
