# DEPLOYMENT.md - ビルド & リリース手順

## 1. ビルドコマンド
```bash
# プロダクション用ビルド
npm run build

# ビルド成果物のローカルプレビュー
npm run preview
2. リリース前品質ゲート (Quality Gates)
[ ] TypeScript の型チェック（tsc --noEmit）がエラーなしで完了すること。
[ ] Playwright による自動テストがすべて全件パス（Pass）すること。
[ ] Vite によるビルド成果物（dist/）が正常に生成されていること。
