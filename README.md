# pull_requestの練習リポジトリ
[リンクの文字](リンク)
[Markdownで行こう！](https://gist.github.com/wate/7072365)

## git -> Githubへのpush（流れ）
1. ローカル上でデイレクトリ作成（プロジェクト）
2. ディレクトリ内で`git init`コマンドを使い初期化
3. 何かしたの作成 or 編集
4. 更新したものをステージングエリアに上げる
5. `git commit -m "コメント"`で変更を保存する
6. Github上でリモートリポジトリを作成
7. git remote add と git pushのコマンドをコピー
8. `git remote add origin git hubのurl`コマンドでローカルとリモートを接続
9. `git push -u origin master`コマンドで保存したソースコードをリモートへ送る

## pullの流れ
1. リモートリポジトリをローカルリポジトりより育てる
2. `git pull origin master`コマンドでリモート上の最新リポジトリをローカルに持ってくる  

## pull Requesrtの流れ
1. `git checkout -b ブランチ名`コマンドで新規ブランチを作成（同時にブランチの切り替えも行ってくれる）
2. 何かしらのアップデートをする
3. `git add .`git commit -m "コメント"`の順で保存する
4. `git push origin 新しいブランチ名`コマンドでリモート上に新しくブランチを作成してpush

### ブランチの切り替え方
+ `git checkout ブランチ名`コマンドでブランチを行き来できる
    + 現在いるランチ上で何かしたらの変更を行っていた場合はその変更内容を保存もしくは削除してからブランチを切移動すること
