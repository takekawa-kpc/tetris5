# PATTERNS.md - 実装パターン & コーディング規約

## 1. AIエージェント出力規約
- **解説は最小限**: コードの背景や説明文章は省略し、要点のみにとどめる。
- **即時実行コマンド**: 必要なコマンド（`npm run dev`, `npx playwright test` 等）を回答の最上部に提示する。
- **修正済みコード優先**: 差分だけでなく、そのままファイルに置き換え可能な完全なコードブロックを出力する。

## 2. Tailwind CSS & テーマ実装パターン
- **ダークモード設定クラス**:
  ```tsx
  <div className="bg-white text-slate-900 dark:bg-slate-900 dark:text-slate-100 transition-colors duration-200">
    {/* コンポーネント実装 */}
  </div>
  ```
- アニメーションクラス標準: transition-all duration-300 ease-in-out や animate-fade-in などのパターンを統一利用する。

## 3. React コンポーネント規約
- 原則として TypeScript の型定義を備えた Function Component として記述する。



追記

## 4. 入力インターフェースパターン（PCキーボード）
- **操作割当**:
  - `ArrowLeft` / `ArrowRight`: 左右移動
  - `ArrowDown`: ソフトドロップ
  - `ArrowUp` または `KeyZ` / `KeyX`: 回転
  - `Space`: ハードドロップ
- **デフォルト挙動の抑止**: 矢印キーやスペースキー押下時に `e.preventDefault()` を呼び出し、ブラウザのスクロールを防ぐこと。
