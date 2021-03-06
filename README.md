# CI_tester

## GitHubアクションを試してみる

- [公式のドキュメント](https://help.github.com/ja/actions)

> GitHubの API やパブリックに利用可能なサードパーティAPIとのインテグレーションなど、好きな方法でリポジトリを操作するカスタムコードを書いて、アクションを作成することができます。 たとえば、アクションでnpmモジュールを公開する、緊急の問題が発生したときにSMSアラートを送信する、本番対応のコードをデプロイすることなどが可能です。

- [ペパボテックブログ](https://tech.pepabo.com/2020/03/11/github-actions-for-lolipop-and-heteml/)がかなり詳しいので自分のサーバーとドメインでためす

### GitHubアクションについて調べる

- GitHubのリポジトリ上でタスクを管理してアクションを実行できる（ワークフロー）
- これを応用するとCI/CDに活用できる

> ワークフローは、Linux、macOS、Windows、コンテナで、'ランナー'と呼ばれるGitHubがホストするマシン上で実行できます。 あるいは、自分が所有もしくは管理するマシン上でワークフローを実行するために、独自にランナーをホストすることもできます。

- ワークフローの作成には公開されているDockerコンテナイメージを利用することができるので、自分で一から作成しなくても良い

>ワークフローの作成には、リポジトリで定義されているアクション、GitHubのパブリックリポジトリにあるオープンソースのアクション、または公開されているDockerコンテナイメージを使用できます。

- [ワークフローの作り方](https://help.github.com/ja/actions/configuring-and-managing-workflows/configuring-a-workflow)
  - 基本はリポジトリトップに`.github/workflows` というディレクトリを作る
  - ディレクトリ内にワークフローの記述のための `.yml` または `.yaml` ファイルを作成
- パッケージを作ったら公開もできる