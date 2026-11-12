---
slug: ja-jp/real-world-development/cloud
title: "GitHub Copilot cloud agent"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

[**GitHub Copilot cloud agent**](https://docs.github.com/copilot/concepts/agents/cloud-agent/about-cloud-agent) を使うと、GitHub Copilot がクラウドで非同期に作業できます。GitHub で作業を割り当てると、cloud agent がバックグラウンドでリポジトリを調査して変更を加え、pull request を作成します。その間、別の作業を続けられます。

これらの演習では、cloud agent が従う custom instruction を追加し、GitHub issue を割り当てて実装を依頼します。custom agent を確認して使い、作業方針を調整します。agents dashboard からセッションを監視して指示し、最後に pull request をレビューして結果を反復的に改善します。

## 演習

| 演習 | トピック | 説明 |
|----------|-------|-------------|
| [0. 前提条件][ex0] | セットアップ | リポジトリと codespace を作成します |
| [1. Custom instruction][ex1] | コンテキスト | cloud agent が従う custom instruction を追加します |
| [2. Cloud agent][ex2] | 非同期エージェント | issue を GitHub Copilot cloud agent に割り当てます |
| [3. Custom agent][ex3] | 特化型エージェント | custom agent を確認して使用します |
| [4. エージェントの管理][ex4] | モニタリング | エージェント セッションを監視して指示します |
| [5. 反復][ex5] | レビュー | pull request をレビューし、Copilot の作業を反復して、次のステップを選びます |

## 前提条件

このワークショップに参加する前に、次の準備をしてください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] アカウントまたは組織で GitHub Copilot cloud agent が有効になっていること

> [!TIP]
> 有料プランを利用していませんか？認証済みの学生は [GitHub Education][callout-student-plan-education] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用する agent、MCP、コードレビュー、Copilot CLI が含まれているため、すべての演習を完了できます。

[callout-student-plan-education]: https://github.com/education/students

> [!NOTE]
> Cloud agent は **Copilot Student、Pro、Pro+、Business、Enterprise** で利用できます。Copilot Free は対象外です。Copilot Business または Enterprise では、管理者が組織で有効にする必要があります。

> [!NOTE]
> このコースでは MCP を扱いません。Copilot で MCP サーバーを使う方法については、[CLI コース][cli]または [VS Code コース][vscode]を参照してください。

## 開始する

**[演習 0: 前提条件から開始 →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-custom-instructions/
[ex2]: 2-cloud-agent/
[ex3]: 3-custom-agents/
[ex4]: 4-managing-agents/
[ex5]: 5-iterating/
[cli]: ../cli/
[vscode]: ../vscode/
