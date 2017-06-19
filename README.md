# typescript-instead-of-babel

TypeScript を、Babel のような JavaScript トランスパイラとして使用する例です。

## 使い方

初めに、次のコマンドを実行して、依存パッケージをインストールしてください。

```sh
yarn
```

次のコマンドを実行すると、`src` ディレクトリ内の JavaScript や TypeScript ファイルを ES3 にトランスパイルした結果が、`dist` ディレクトリに保存されます。

```sh
yarn run build
```

次のコマンドを実行すると、実行を中止するまで、`src` ディレクトリ内の JavaScript や TypeScript ファイルを保存する度に、それらを ES3 にトランスパイルした結果が、`dist` ディレクトリに保存されます。

```sh
yarn run watch
```

次のコマンドを実行すると、`dist` ディレクトリを削除します。

```sh
yarn run clean
```

## 解説

`tsconfig.json` の一部をデフォルトの設定から変更しています。変更箇所は、次のとおりです。

```json
{
  "compilerOptions": {
    "target": "es3",      /* ES3 に変換します。(デフォルト: "es5") */
    "allowJs": true,      /* JavaScript ファイルも変換の対象にします。(デフォルト: false) */
    "outDir": "./dist",   /* 変換先のディレクトリを指定します。(デフォルト: "./") */
    "rootDir": "./src",   /* 変換元のディレクトリを指定します。(デフォルト: "./") */
  }
}
```
