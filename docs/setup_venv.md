# venvによる仮想環境
本ページでは、Python公式版にデフォルトで入っている`venv`モジュールを使用し、軽量な仮想環境の作成を行います。
!!! warning
    この記事で紹介する`venv`は、Python公式版のみ対応しています。  
    Anaconda版では、`conda`コマンドで生成できる仮想環境があるので、Anacondaを使う人はそちらを使用してください。

## venvの使い方
### 新しく環境を作成
`venv`による仮想環境は、卒論・修論等のプロジェクトごとに作るようにして下さい。  
なお、`venv`の仮想環境はコマンドを実行したときのワークスペース（作業フォルダ）に生成されます。

ターミナルで、以下のコマンドを実行します。
```bash title="Terminal or Command Prompt"
python -m venv [envname]     # [envname]は、わかりやすい仮想環境名を入れること
```
### 環境のActivate
仮想環境に入る際に使うコマンドです。
#### Linux, Macの場合
以下のどちらかを実行
```bash title="Terminal"
source [envname]/bin/activate
```
```bash title="Terminal"
. [envname]/bin/activate
```

#### Windowsの場合
以下を実行
```bash title="Command Prompt"
.\[envname]\Scripts\activate
```

すると、ターミナルの表示が

Before: 
`C:\Users\fumiy\Python_Lecture>  # 仮想環境に入る前`  
After: 
`([envname]) C:\Users\fumiy\Python_Lecture>  # 仮想環境に入った後`

のように変わります。
作業ディレクトリを書いているところに`([envname])`というのが先頭に追加されましたね、これで仮想環境に入れました。
あとは、この環境でいつもと同じように作業を行えばOKです。

### 環境のDeactivate
仮想環境から出る際に使うコマンドです。
```bash title="Terminal or Command Prompt"
deactivate
```

## まとめ
- 仮想環境は、プロジェクトごとに作るようにしましょう。
- 仮想環境に入るときは、`source [envname]/bin/activate`または`.\[envname]\Scripts\activate`を実行しましょう。
- 仮想環境から出るときは、`deactivate`を実行しましょう。

このほかにも、仮想環境については様々な機能があります。
詳しくは、[公式ドキュメント](https://docs.python.org/ja/3/library/venv.html)を参照してください。

また、最近ではPoetryというツールが流行っているようです。
こちらも、興味があれば調べてみてください。  
時間があれば、Poetryについても記事を書きたいと思います。