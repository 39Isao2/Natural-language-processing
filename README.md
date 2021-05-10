# 自然言語処理について

## 自然言語処理とは？
そもそも「自然言語」とは私たちが普段話している日本語や英語などの言語のことです。<br>
具体的な処理ですが、まず形態素解析といって文章を可能な限り小さい単位（名詞、動詞、助詞など）に分割することから始まり、次にかがり受けなどの構造を明らかにする構文解析を行います。<br>
そして最後に文の中で「誰がいつどこで何をした」という5W1Hを意味解析で判定します。<br>

<img src="img/flow.png" width="600px"><br>
参考:https://qiita.com/cr-fun/items/cc82a85c572daac0b5c5

## jupyter notebookのインストール
「Jupyter Notebook」は、PythonなどをWebブラウザ上で記述・実行できる統合開発環境です。<br>
「ジュピターノートブック」、「ジュパイターノートブック」と読みます。 

**Anaconda（Pythonのライブラリが豊富に含まれた環境）** と一緒にインストールします。 
https://www.anaconda.com/products/individual <br>

<img src="img/jy.png" width="800px"><br>

new → Folder から フォルダを作成 → チェックボックスにチェックを入れてRenameして「jupyter」というフォルダ名に変更<br><br>

続いて、新規のノートブックを作成します。「jupyter」フォルダに移動後、「New」から「Python3」をクリックして、新規ノートブックを作成します。<br>

<img src="img/nt.png" width="800px"><br>


## 実践（形態素解析）

事前にコマンドプロンプトで「janome」ライブラリをインストール
```
pip install janome

```

```
from janome.tokenizer import Tokenizer

t = Tokenizer()

s = "私はご飯を食べる。そして学校へ行く。"

for token in t.tokenize(s):
    print(token)
    
```
