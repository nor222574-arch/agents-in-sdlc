---
slug: ja-jp/real-world-development/cli
title: "GitHub Copilot CLI"
description: "Copilot CLI のモード、カスタマイズ、MCP ツール、pull request の自動化を学びながら、Tailspin Toys に 2 つの変更を加え、検証してリリースします。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

**[GitHub Copilot CLI][about-copilot-cli]** は、ターミナルで GitHub Copilot をエージェント型のコーディング アシスタントとして利用できるようにします。コードベースを探索し、コードを生成し、コマンドを実行し、外部ツールに接続できます。すべてコマンド ラインから行えるため、グラフィカル エディターに切り替えずに作業の流れを保てます。

このワークショップでは、Tailspin Toys を使って一連の流れを進めます。

1. GitHub Codespaces でプロジェクトを準備し、Copilot CLI をインストールして基本を確認します。
2. 星評価の小さな変更を加え、ブラウザーで確認し、最初の pull request (PR) を手動でマージします。
3. フィルターの issue から始め、Plan モードで方針を決め、Autopilot モードで実装し、Interactive モードでレビューします。
4. リポジトリの instruction を更新し、フィルターの作業に適用します。
5. 既存の `quality-checks` skill をカスタマイズして、プロジェクトのチェックを実行します。
6. Playwright Model Context Protocol (MCP) サーバーを追加し、ブラウザーでフィルターの動作を確認します。
7. QA (品質保証) custom agent を作成し、要件、テスト範囲、検証結果をレビューします。
8. フィルターの変更全体をレビューし、その PR で Agent Merge を使用します。
9. コンテキスト、モデル、共有、任意の cloud delegation に使える slash command を確認します。

内容に集中できるよう、PR は 2 件作成します。1 件目は星評価、2 件目は instruction の更新、skill の更新、QA profile、テストを含むフィルター機能です。フィルターと品質のワークフローでは、1 つの会話とブランチを共有するため、各ツールを試しながら作業を積み重ねられます。

## レッスン

| レッスン | トピック | 説明 |
| ------ | ----- | ----------- |
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成します |
| [1. Copilot CLI のインストール][ex1] | インストール | Copilot CLI をインストールして認証し、基本を確認します |
| [2. 星評価を追加する: 手軽な改善][ex2] | 最初の変更 | 既存の評価と null の場合の代替表示を確認し、最初の PR をマージします |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | issue から機能を計画し、Autopilot で実装して Interactive でレビューします |
| [4. カスタム instruction で Copilot を導く][ex4] | コンテキスト | instruction を確認して更新し、フィルターに適用します |
| [5. quality-checks skill をカスタマイズして使う][ex5] | 繰り返し可能なチェック | 既存の skill を確認し、レポート形式を変更して実行します |
| [6. Playwright MCP で機能を検証する][ex6] | ブラウザーでの確認 | CLI で MCP を設定し、フィルターの動作を確認します |
| [7. QA agent を作成して使う][ex7] | 要件とテスト範囲 | 専門 profile を作成して選択し、最終検証の結果を集めます |
| [8. 機能 PR を作成してマージする][ex8] | レビューとマージ | 変更全体をレビューして PR を作成し、Agent Merge を使います |
| [9. GitHub Copilot CLI の slash command][ex9] | CLI 機能 | コンテキスト、モデル、共有、cloud agent への任意の委任を確認します |
| [10. まとめと次のステップ][ex10] | まとめ | ワークフロー、再利用可能なカスタマイズ、参考資料を確認します |
| [オプション: Foundry を組み込む][foundry] | ホスト型エージェント | モデルを準備し、カタログに基づいたエージェントをデプロイして Web サイトに接続します |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] リポジトリと Codespace を作成する権限
- [ ] ターミナルまたはコマンド ライン操作の基本的な知識

> [!TIP]
> 有料プランを利用していませんか？認証済みの学生は [GitHub Education][student-plan] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使う agent、MCP、コードレビュー、Copilot CLI の機能が含まれています。

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合は、管理者が Copilot CLI を有効にしていることを確認してください。

## 開始する

**[前提条件から開始 →][ex0]**

[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[student-plan]: https://github.com/education/students
[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
