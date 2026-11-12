---
title: "レッスン 12 - GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot app で Pages ワークフローを設定し、その pull request をレビューして、公開された Space Quiz を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

GitHub Pages で Space Quiz をデプロイし、誰でもアクセスできるようにします。Copilot はワークフローの準備とデプロイの案内を行えますが、変更をレビューし、サイトが公開されたことを確認するのはユーザーの役割です。

このレッスンでは、次のことを行います。

- Copilot に GitHub Pages のデプロイ設定を依頼します。
- マージする前にワークフローと pull request をレビューします。
- デプロイの進行状況を確認し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、手軽に試す方法が必要です。単一ファイルのサイトを GitHub Pages で公開すれば、サーバーやランタイム依存関係を追加せずに、パブリック URL から利用できるようになります。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot app セッションで、次のプロンプトを送信します。

```plaintext
このリポジトリで GitHub Pages を有効にしてください。必要に応じて Web サイトをビルドし、GitHub Pages にデプロイする GitHub Actions ワークフローを作成してください。README がまだない場合は、アプリの説明とローカルでの実行方法を記載した README を追加してください。これらの変更で pull request を作成し、必須チェックに合格したらマージしてください。デプロイが成功するまで監視し、最後に公開された Web サイトの URL を報告してください。Pages の有効化やマージの権限がない場合は、何を承認または実行する必要があるかを正確に説明してください。サイトが実際に公開されるまで、成功したと報告しないでください。
```

![3 段階の図。space-quiz の pull request がマージされた状態、Build website、Upload artifact、Deploy to Pages の各ステップが成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz を示します。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントに pull request の作成とマージ、およびリポジトリの Pages 設定変更を依頼します。続行する前に、差分、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローをレビューしてデプロイを確認する

1. リポジトリに README がない場合に限り、README が追加されていることを確認します。
2. ワークフローのビルドとデプロイの手順を含め、pull request の変更をレビューします。
3. 必須の pull request チェックに合格した後にのみマージします。
4. GitHub Actions のデプロイ実行が成功するまで確認します。
5. 報告された URL を開き、Space Quiz が表示されることを確認します。

エージェントが Pages を有効にできない場合や pull request をマージできない場合は、提示された具体的な手順に従います。デプロイが成功し、公開サイトが読み込まれるまではタスクを完了扱いにしないでください。

## まとめと次のステップ

Space Quiz が公開サイトとして利用可能になり、エージェントの報告だけに頼らずデプロイを確認できました。次は[レッスン 13: レビューと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
