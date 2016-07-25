# CLIアプリケーション作成用テンプレート(Python)

PythonでCLIアプリケーションを作成するためのテンプレートです。

[app/app.py](app/app.py)を編集することでCLIアプリケーションを作成することができます。

このテンプレートではCLI作成のユーティリティとして、`argparse`を使用しています。  
（詳細は[公式ドキュメント](https://docs.python.org/2.7/library/argparse.html)をごらんください。）

## 引数の取得
[app.py](app/app.py)では`main`という関数が定義されています。

``` python
def main(args, options):
```

コマンドライン引数は`args`に配列として渡されます。  
オプション形式の引数を使用する場合はargparseの`parser.add_argument`にoption引数を追加してください。([cli.py](cli.py))

## 結果の出力
コマンド実行結果の標準出力への出力は標準の`print`メソッドを使用してください。

``` python
  print(result)
```

## 外部ライブラリの追加方法
外部ライブラリを使用する場合は以下の手順でおこなってください。

- [requirements.txt](requirements.txt)にライブラリ名とバージョンを記述
- [codecheck.yml](codecheck.yml)に以下の内容を追加：

``` yaml
build:
  - pip install -r requirements.txt
```
