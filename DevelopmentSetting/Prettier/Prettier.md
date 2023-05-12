# Prettier

[Prettier](https://www.npmjs.com/package/prettier)とはコードフォーマッター（ソースコードを整形してくれるツール）のこと。

ソースコードの品質を保つために使用される。

ドキュメント記載時のバージョンはこちら。

* Prettier
  * 2.8.7
* ESLint
  * 8.24.0
* Stylelint
  * 15.4.0

## 利用方法

### インストール

以下のコマンドを入力してパッケージをインストールする。

```bash
npm i -D prettier
```

### .prettier.json

Prettierの設定ファイル。

設定を記述することでデフォルトの設定を上書きできる。

```json
{
  "singleQuote": true
}
```

指定可能なオプションやファイルの形式は[こちら](https://prettier.io/docs/en/options.html)を参照。

#### 特定のフォルダーや拡張子で設定を変える

`overrides`を使用すると異なる構成を適用できる。

```json
{
  "overrides": [
    {
      "files": ["*.scss"],
      "options": {
        "singleQuote": false
      }
    }
  ]
}

```

### 実行

以下のコマンドを実行すると整形されたファイルが出力される。

```bash
npx prettier hoge/piyo.js --wite
```

特定のファイルではなく全てのファイルを対象にした場合は以下のコマンドを実行する。

```bash
npx prettier --wite .
```

### 除外設定

一部のファイルでは整形をしたくない場合は`.prettierignore`を作成する。

```
hoge.js
piyo.scss
```

`node_modules`など最初から除外されているものは[こちら]([.prettierignore](https://prettier.io/docs/en/ignore.html#ignoring-files-prettierignore))を参照。

## ESLintとの併用

ESLintでも`eslint --fix`でコードを整形できるが、Prettierの方が整形に優れているので整形はPrettier行う。

しかしESLintにもフォーマットのルールが存在するため、競合する可能性がある。  
そのため、ESLintのフォーマットのルールを無効化してPrettierとESLintを実行できるようにする。

### 併用に必要なパッケージ

以下のコマンドを実行してパッケージをインストールする。

```bash
npm i -D eslint eslint-config-prettier
```

パッケージの詳細は以下の通り。

* `eslint`
  * ESLint本体
* `eslint-config-prettier`
  * ESLintのフォーマット関連のルールを全て無効にする

### ESLintの設定

Prettierに関連する設定を追記する。

```json
{
    "extends": [
        "eslint:recommended",
        "prettier"
    ]
}
```

`prettier`の記述は必ず`extends`配列内の最後に記述する。

## Stylelintとの併用

ESLintと同様にフォーマットのルールが競合していたが、v15から書式ルールが非推奨になったため、そのまま併用可能。
