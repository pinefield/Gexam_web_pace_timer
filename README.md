# G検定 ペースタイマー

シンプルなブラウザ用ペースタイマーです。指定時間（既定: 9/6 13:00–15:00）の進行度に応じて、
- 現在時刻
- 残り時間
- 平均回答ペース（目安）
- 進捗バー
を表示します。

## デモ（GitHub Pages）
GitHub Pages を有効化すると、次のURLで公開されます。

- 例: https://pinefield.github.io/Gexam_web_pace_timer/

有効化手順は下記「GitHub Pages」を参照してください。

## 使い方
- `index.html` をブラウザで開くだけで動作します。ビルドは不要です。
- 開始・終了時刻と問題数はファイル先頭付近の定数で設定します。
  - `index.html:34` … `TOTAL_QUESTIONS`
  - `index.html:37` … `START_AT`
  - `index.html:38` … `END_AT`

## デバッグ（現在時刻の手動設定）
画面下部の「デバッグ: 現在時刻を手動設定」で、現在時刻を上書きできます。
- `datetime-local` 入力に日付時刻を指定すると、その時刻を起点に実時間の経過分だけ仮想時刻が進みます。
- 設定値は `localStorage` に保存され、ページ再読み込み後も維持されます。
- 「今に戻す」ボタンで解除（実時刻に復帰）できます。

## GitHub Pages
プロジェクトの `main` ブランチのルートから配信する設定がおすすめです。
- GitHub のリポジトリ画面 → `Settings` → `Pages`
  - `Source`: `Deploy from a branch`
  - `Branch`: `main` / `/ (root)` を選択し `Save`
- 反映後、`https://<GitHubユーザー名>.github.io/<リポジトリ名>/` で公開されます。
- 本リポジトリでは Jekyll を無効化するために `.nojekyll` を同梱しています。

## 開発メモ
- 依存なし（HTML + CSS + JS のみ）
- ローカル動作確認: そのままブラウザで開く or 簡易サーバー（例: `python -m http.server`）

## リポジトリ情報（提案）
- 説明: 「G検定向けのシンプルなペースタイマー。現在時刻・残り時間・目安ペースを表示。デバッグで時刻上書き可能。」
- トピック例: `timer`, `countdown`, `exam`, `github-pages`, `javascript`, `japanese`, `progress`
