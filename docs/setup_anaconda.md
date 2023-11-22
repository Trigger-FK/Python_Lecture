# Anacondaの環境構築
このページでは、Anacondaの環境構築について説明します。
!!! note
    このページでは、Anacondaのインストール方法を説明します。
    Python公式版をインストールしたい場合は、[こちら](setup_python.md)を参照してください。

## 前提条件
**Anacondaは、日本語などを含むフォルダにはインストールできません。**  
Windowsの人はAnacondaの環境構築を行う前に、**ユーザ名が日本語でないこと**を確認してください。

ユーザ名の確認方法は、以下の通りです。

1. コマンドプロンプトを開く
1. `whoami`と入力して、`Enter`を押す  

すると、以下のような表示が出ます。
    ```bash title="コマンドプロンプト"
    C:\Users\[ユーザ名]>whoami
    [ユーザ名]
    ```
このとき、`[ユーザ名]`が日本語でないことを確認してください。  
もし日本語だった場合は、インストール方法が少し異なります。

## Anacondaのインストール
[Anacondaの公式サイト](https://www.anaconda.com/products/individual)から、PCのOSに合わせたインストーラをダウンロードしてください。

### Windows, Macの場合
インストーラをダブルクリックして、指示に従ってインストールを行ってください。

ユーザ名が日本語だった場合は、[公式サイトのインストール方法](https://www.python.jp/install/anaconda/windows/install.html)を参考にしてください。

!!! warning
    Windowsの場合、インストール時に「Add Anaconda to my PATH environment variable」という項目がありますが、**チェックを入れないでください。**  
    これをチェックすると、Anacondaの環境がPC全体に影響を与えるため、他のアプリケーションに影響を与える可能性があります。  
    また、チェックを入れない場合でも、Anacondaの環境を使うことは可能です。

!!! note
    インストール時に「Install for me only」か「Install on this location」かを選択する画面が出ますが、**「Install for me only」を選択してください。**

### Linuxの場合
ダウンロードしたインストーラをターミナルで実行します。
```bash title="Terminal"
cd Downloads  # ダウンロードしたファイルがあるディレクトリに移動してください
bash Anaconda3-202x.xx-Linux-x86_64.sh  # ダウンロードしたファイル名に合わせてください
```
すると、以下のような表示が出るので、`Enter`を押してください。
```bash title="Terminal"
Welcome to Anaconda3 202x.xx

In order to continue the installation process, please review the license
agreement.
Please, press ENTER to continue
>>>
```
次に、ライセンスに同意するかどうかを聞かれるので、`yes`と入力してください。
```bash title="Terminal"
Do you accept the license terms? [yes|no]
[no] >>> yes
```
次に、インストール先を聞かれるので、`Enter`を押してください。
```bash title="Terminal"
Anaconda3 will now be installed into this location:

/home/usename/anaconda3

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below

[/home/usename/anaconda3] >>>
```
すると、インストールが始まります。  
インストールが完了すると、以下のような表示が出るので、`Enter`を押してください。
```bash title="Terminal"
...
installation finished.
Do you wish the installer to initialize Anaconda3
by running conda init? [yes|no]
[no] >>> yes

no change     /home/usename/anaconda3/condabin/conda
no change     /home/usename/anaconda3/bin/conda
no change     /home/usename/anaconda3/bin/conda-env
no change     /home/usename/anaconda3/bin/activate
no change     /home/usename/anaconda3/bin/deactivate
no change     /home/usename/anaconda3/etc/profile.d/conda.sh
no change     /home/usename/anaconda3/etc/fish/conf.d/conda.fish
no change     /home/usename/anaconda3/shell/condabin/Conda.psm1
no change     /home/usename/anaconda3/shell/condabin/conda-hook.ps1
no change     /home/usename/anaconda3/lib/python3.8/site-packages/xontrib/conda.xsh
no change     /home/usename/anaconda3/etc/profile.d/conda.csh
modified      /home/usename/.bashrc

==> For changes to take effect, close and re-open your current shell. <==
```
最後に、ターミナルを再起動してください。  

さて、Anacondaのインストールは以上です。
最後の最後に、Anaconda Navigatorが起動できることを確認してください。
起動できたら、インストールは成功です。

### Jupyter LabとJupyter Notebook
Anaconda Navigatorには、色んなツールが同梱されています。
その中で、AnacondaでPythonを使う際に最も重要なのが、**Jupyter Lab**と**Jupyter Notebook**です。

これらは、ブラウザ上でPythonのコードを実行できるアプリケーションです。  
違いは、Jupyter Labの方が機能が豊富で、Jupyter Notebookはシンプルな操作性を持っている点ぐらいですね。
なので、気にせずお好きな方を使ってください。

まぁ、**僕は圧倒的にJupyter Lab派**ですが。  
気にせずお好きな方を（2回目）。

Jupyter LabとJupyter Notebookは、Anaconda Navigatorから起動できます。

!!! note
    Jupyter LabとJupyter Notebookを開いたとき、デフォルトでユーザフォルダが開かれます。  
    このフォルダに、Jupyter LabとJupyter Notebookで作成したファイルが保存されます。

    もし別フォルダに保存したい場合は、`New Folder`でフォルダを生成し、そのフォルダ内で作業を行ってください。

Jupyter LabとJupyter Notebookは通常の`.py`ではなく、`.ipynb`という拡張子のファイルで保存されます。
これは、Jupyter LabとJupyter Notebookのファイル形式で、Pythonのコードを記述することができます。
また、コードがブロックごとに書くことができ、各ブロックごとに実行することが可能です。

## まとめ
- Anaconda Navigatorから、Jupyter LabとJupyter Notebookを起動できる
- Jupyter LabとJupyter Notebookは、ブラウザ上でPythonのコードを実行できるアプリケーション
- 保存場所を変更したいときは、`New Folder`でフォルダを生成するかフォルダを移動し、そのフォルダ内で作業を行う
- 執筆者はJupyter Lab派

（余談）ちなみに、VSCodeでもJupyter LabとJupyter Notebookのファイルを開くことができます。