# CLIアプリケーション作成用テンプレート(Python)

PythonでCLIアプリケーションを作成するためのテンプレートです。

[app/app.py](app/app.py)を編集することでCLIアプリケーションを作成することができます。

このテンプレートではCLI作成のユーティリティとして、argparseを使用していsます。  
argparseについての詳細は[公式ドキュメント](https://docs.python.org/2.7/library/argparse.html)をごらんください。

## コマンドライン引数の取得方法
app.pyでは`main`という関数が定義されています。

``` python
def main(args, options):
```

パラメータは`args`に配列として渡されます。  
オプション形式の引数を使用する場合はargparseでoption引数を追加してください。([cli.py](cli.py))

## コマンド実行結果の標準出力への出力
標準の`print`メソッドを使用してください。

``` python
  print(v)
```

## 外部ライブラリの追加方法
外部ライブラリを使用する場合は以下の手順でおこなってください。

- requirments.txtにライブラリ名とバージョンを記述
- codecheck.ymlに以下の内容を追加

``` yaml
build:
  - pip install -r requirements.txt
```
