# git-flow

git-flowとはGitのブランチ機能を利用する開発戦略。  
効率的に開発するソースコードを管理することが目的。

## コマンド

各フロー実行時に入力するコマンドは以下の通り。

### featureブランチで機能開発

featureブランチを`start`コマンドを使って作成。

```bash
git flow feature start <feature name>
```

`finish`コマンドでdevelopにマージ。

```bash
git flow feature finish <feature name>
```

### releaseブランチでリリースを準備

releaseブランチを`start`コマンドを使って作成。

```bash
git flow release start <version>
```

`finish`コマンドでmain, developにマージ。

```bash
git flow release finish <version>
```

### リリース後のバグ対応

hotfixブランチを`start`コマンドを使って作成。

```bash
git flow hotfix start <version>
```

`finish`コマンドでmainにマージ。

```bash
git flow hotfix finish <version>
```
