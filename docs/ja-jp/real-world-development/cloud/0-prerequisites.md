---
title: "演習 0: 前提条件"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

Copilot cloud agent の演習を始める前に、必要な準備をします。Tailspin Toys リポジトリのコピーを作成し、instruction file の編集や cloud agent の作業レビューに使う [codespace][codespaces] を起動します。

## 演習用リポジトリをセットアップする

コードを作成するためのリポジトリのコピーとして、[テンプレート リポジトリ][template-repository]からインスタンスを作成します。新しいインスタンスには演習に必要なファイルがすべて含まれます。各演習でこのリポジトリを使用します。

1. 新しいブラウザー ウィンドウで [Tailspin Toys のテンプレート][tailspin-template]を開きます。
2. 演習用リポジトリのページで **Use this template** を選択し、リポジトリのコピーを作成します。次に **Create a new repository** を選択します。

    ![Use this template ボタン](../../../_images/ex0-use-template.png)

3. GitHub または Microsoft が主催するイベントでワークショップに参加している場合は、メンターの指示に従います。それ以外の場合は、GitHub Copilot を利用できる組織に新しいリポジトリを作成できます。

    ![テンプレート リポジトリの設定](../../../_images/ex0-repository-settings.png)

4. 後で参照するため、作成したリポジトリのパス（**organization-or-user-name/repository-name**）を控えておきます。

## codespace を作成する

次に、演習を完了するための codespace を用意します。

[GitHub Codespaces][codespaces] は、ブラウザーで直接コードの作成、実行、デバッグができるクラウドベースの開発環境です。複数のプログラミング言語、拡張機能、ツールをサポートする、機能豊富な IDE を提供します。

1. 新しく作成したリポジトリを開きます。
2. 緑色の **Code** ボタンを選択します。

    ![Code ボタンを選択](../../../_images/ex0-code-button.png)

3. **Codespaces** タブを選択し、**+** ボタンを選択して新しい codespace を作成します。

    ![新しい codespace を作成](../../../_images/ex0-create-codespace.png)

codespace の作成には数分かかりますが、すべてのサービスを手動でインストールするよりもはるかに短時間で済みます。その間に GitHub Copilot のほかの機能を確認してみましょう。次のレッスンで取り上げます。

> [!CAUTION]
> 後の演習で codespace に戻ります。今はブラウザーのタブで開いたままにしてください。

> [!NOTE]
> このワークショップは codespace またはローカルの [dev container][dev-containers] で実行できます。どちらも、スムーズに進めるために必要な前提条件がすべてインストールされた環境です。ローカルで実行する場合は、クローンしたリポジトリを VS Code で開き、プロンプトが表示されたら **Reopen in Container** を選択します。codespace と同じ dev container が VS Code によって構築されます。

[codespaces]: https://github.com/features/codespaces
[dev-containers]: https://code.visualstudio.com/docs/devcontainers/containers

## まとめ

おめでとうございます。演習用リポジトリのコピーを作成し、Copilot cloud agent と作業するための codespace の作成を開始しました。

## 次のステップ

cloud agent が従う custom instruction を追加します。[演習 1 - Custom instructions][next-lesson]に進みます。

## リソース

- [GitHub Codespaces の概要][codespaces]
- [テンプレートからリポジトリを作成する][template-repository]
- [Codespaces を使い始める][codespaces-quickstart]

[tailspin-template]: https://github.com/github-samples/tailspin-toys
[template-repository]: https://docs.github.com/repositories/creating-and-managing-repositories/creating-a-template-repository
[codespaces-quickstart]: https://docs.github.com/codespaces/getting-started/quickstart
[next-lesson]: ../1-custom-instructions/
