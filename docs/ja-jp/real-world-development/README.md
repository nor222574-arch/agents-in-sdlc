---
title: "実践的な開発"
slug: ja-jp/real-world-development
authors:
  - geektrainer
lastUpdated: 2026-09-16
---

現実的なシナリオ、完成したアプリケーション、共有バックログを使って、ソフトウェア開発ライフサイクル全体で GitHub Copilot を活用します。変更の計画、コードの作成、動作のテスト、pull request のレビュー、エージェントによる作業管理を繰り返し行います。

## シナリオ

開発者向けテーマのボードゲーム クラウドファンディングを提供する架空の会社、Tailspin Toys の新しい開発者として参加します。チームのバックログは GitHub issue として登録済みで、すぐに着手できます。フィルターやページネーションなどの機能開発に加え、アクセシビリティやコーディング標準などの品質改善も含まれています。

## 作業環境を選ぶ

GitHub Copilot はさまざまな作業環境で利用できます。自分の開発スタイルに合う環境を選びます。各ワークショップは独自のセットアップから始まり、共通の Tailspin Toys シナリオを使用します。

### [GitHub Copilot CLI][cli]

ターミナルでエージェント型アシスタントを使います。Plan モードと Autopilot モード、instruction、skill、カスタム エージェント、Playwright MCP、Agent Merge、便利なスラッシュ コマンドを扱います。

### [GitHub Copilot app][app]

エージェント セッションを並行して実行し、セッション モードを切り替え、canvas で共同作業し、デスクトップ アプリで GitHub issue と pull request を管理します。

### [GitHub Copilot cloud agent][cloud]

GitHub issue を非同期エージェントに割り当てて作業を導き、進捗を監視し、エージェントが作成する pull request をレビューします。

### [Visual Studio Code][vscode]

Visual Studio Code と GitHub Codespaces で GitHub Copilot を使用します。エディターを離れずに、Copilot Chat の agent mode、MCP サーバー、カスタム エージェントを活用します。

[cli]: cli/
[app]: app/
[cloud]: cloud/
[vscode]: vscode/
