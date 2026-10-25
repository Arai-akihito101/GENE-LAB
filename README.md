# GENE LAB Ver.1.4.1 — 公開サイトの動作修正

## 修正内容

Ver.1.4の `index.html` 内で「実験結果を格納する配列 history」と「ブラウザの window.history」を取り違えていた問題を修正しました。

公開サイト（HTTP/HTTPS）では初期表示時の `select()` が `history.replaceState is not a function` で例外となり、画面の操作・テーマ切替などが正常に初期化されないことがありました。

`window.history.replaceState(...)` に修正し、その他の機能・12テーマ・解説ページとシンプルな花デザインはそのままです。

## 更新方法

GitHubの `gene-lab` リポジトリのルートにある `index.html` を、このZIP内の `index.html` に差し替えてコミットしてください。**既にある `/learn/` 以下は削除不要です。**

ZIPには解説ページやrobots.txt、sitemap.xmlも同梱しています。全フォルダを上書きしても使えます。

## 備考

公開後に旧ページが残る場合は、ハードリロード（Ctrl+Shift+R）やプライベートウィンドウで確認してください。
