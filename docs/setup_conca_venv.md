# condaによる仮想環境
本ページでは、Anacondaに付属しているcondaを使用し、軽量な仮想環境の作成を行います。

!!! warning
    この記事で紹介するcondaは、Anaconda版のみ対応しています。  
    Python公式版では、venvモジュールを使用して仮想環境を作成するので、Python公式版を使う人はそちらを使用してください。

## condaの使い方
### 新しく環境を作成
仮想環境は、卒論・修論等のプロジェクトごとに作るようにして下さい。

ターミナルで、以下のコマンドを実行します。
```bash title="Terminal or Command Prompt"
conda create -n [envname] python={version}     # [envname]は、わかりやすい仮想環境名を入れること
```
`{version}`には、使用したいPythonのバージョンを入れてください。

### 環境のActivate
仮想環境に入る際に使うコマンドです。
```bash title="Terminal or Command Prompt"
conda activate [envname]
```

すると、ターミナルの表示が
```bash
Before:
(base) C:\Users\fumiy\Python_Lecture>  # 仮想環境に入る前
After:
([envname]) C:\Users\fumiy\Python_Lecture>  # 仮想環境に入った後
```
のように変わります。

作業ディレクトリを書いているところに`([envname])`というのが先頭に追加されましたね、これで仮想環境に入れました。
あとは、この環境でいつもと同じように作業を行えばOKです。

### 環境のDeactivate
仮想環境から出る際に使うコマンドです。
```bash title="Terminal or Command Prompt"
conda deactivate
```

## まとめ
- 仮想環境は、プロジェクトごとに作るようにしましょう。
- 仮想環境に入るときは、`conda activate [envname]`を実行しましょう。
- 仮想環境から出るときは、`conda deactivate`を実行しましょう。
