---
slug: ja-jp/real-world-development/app
title: "GitHub Copilot app"
authors:
  - geektrainer
lastUpdated: 2026-10-22
---

**[GitHub Copilot app](https://docs.github.com/copilot/concepts/agents/github-copilot-app)** は Copilot CLI を基盤としたデスクトップ アプリケーションで、エージェント型開発のための専用ワークスペースを提供します。並列エージェント セッション、切り替え可能なセッション モード、共有 canvas、GitHub issue と pull request のネイティブな管理機能を備えています。また **Agent Merge** は、pull request の rebase、レビュー フィードバック、継続的インテグレーション (CI) の修正、マージを支援します。

このワークショップでは、Tailspin Toys を使って一連の流れを進めます。

1. プロジェクトを準備し、アプリをインストールしてリポジトリに接続し、ワークスペースと初期バックログを確認します。
2. 星評価の小さな変更を加え、ブラウザーで確認し、最初の pull request (PR) を手動でマージします。
3. フィルターの issue から始め、**Plan** モードで方針を決め、**Autopilot** モードで実装し、**Interactive** モードでレビューします。
4. リポジトリの instruction を更新し、フィルターの作業に適用します。
5. 既存の `quality-checks` skill をカスタマイズして、プロジェクトのチェックを実行します。
6. Playwright Model Context Protocol (MCP) サーバーを追加し、ブラウザーでフィルターの動作を確認します。
7. QA (品質保証) custom agent を作成し、要件、テスト範囲、検証結果をレビューします。
8. フィルターの変更全体をレビューし、2 件目の PR で Agent Merge を使用します。
9. canvas が利用可能か確認し、Database Explorer を使った後、リポジトリに接続した triage canvas を作成してテストします。必要な機能を利用できない場合は、ブロッカーを記録し、読み取り専用の代替手段を使うか、まとめに進みます。

内容に集中できるよう、PR は 2 件作成します。1 件目は星評価、2 件目は instruction の更新、skill の更新、QA profile、テストを含むフィルター機能です。それぞれ更新済みの `main` から開始します。フィルターと品質のワークフローでは、1 つのセッション、worktree、ブランチを共有するため、各ツールを試しながら作業を積み重ねられます。最後の canvas 演習は専用セッションで行い、PR の流れを繰り返さずに共有 surface の作成とテストに集中します。

## レッスン

| レッスン | トピック | 説明 |
|--------|-------|-------------|
| [0. 前提条件][ex0] | セットアップ | Node.js をインストールし、Tailspin Toys のコピーを作成します |
| [1. Copilot app のインストール][ex1] | セットアップ | アプリをインストールしてプロジェクトに接続し、ワークスペースを確認します |
| [2. 星評価を追加する: 手軽な改善][ex2] | 最初の変更 | 既存の評価と null の場合の代替表示を確認し、最初の PR をマージします |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | issue から機能を計画し、Autopilot で実装して Interactive でレビューします |
| [4. カスタム instruction で Copilot を導く][ex4] | コンテキスト | instruction を確認して更新し、フィルターに適用します |
| [5. quality-checks skill をカスタマイズして使う][ex5] | 繰り返し可能なチェック | 既存の skill を確認し、レポート形式を変更して実行します |
| [6. Playwright MCP で機能を検証する][ex6] | ブラウザーでの確認 | Customize から MCP を設定し、フィルターの動作を確認します |
| [7. QA agent を作成して使う][ex7] | 要件とテスト範囲 | 専門 profile を作成して選択し、最終検証の結果を集めます |
| [8. 機能 PR を作成してマージする][ex8] | レビューとマージ | フィルター、instruction、skill、QA profile、テストをレビューし、2 件目の PR で Agent Merge を使います |
| [9. canvas を確認して作成する][ex9] | コラボレーション | Database Explorer を使い、リポジトリに接続した triage canvas を作成してテストします |
| [10. まとめと次のステップ][ex10] | まとめ | ワークフロー、成果物、参考資料を確認します |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] **macOS、Linux、Windows** を実行するコンピューター
- [ ] コンピューターに [Git をインストール][install-git]していること

> [!TIP]
> 有料プランを利用していませんか？認証済みの学生は [GitHub Education][callout-student-plan-education] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使う agent、MCP、コードレビュー、Copilot CLI の機能が含まれているため、すべてのコースを完了できます。

> [!NOTE]
> Copilot app は codespace ではなく自分のコンピューターで動作します。そのため、[前提条件の演習][ex0]では、アプリのインストール前に Node.js をインストールしてプロジェクトのコピーを作成します。

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合、管理者は **GitHub Copilot app** ポリシーを有効にしておく必要があります。これは Copilot CLI ポリシーとは別です。

## 開始する

**[前提条件から開始 →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-app/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-canvases/
[ex10]: 10-review/
[install-git]: https://github.com/git-guides/install-git
[callout-student-plan-education]: https://github.com/education/students
