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
3. `git add .`, `git commit -m "コメント"`の順で保存する
4. `git push origin 新しいブランチ名`コマンドでリモート上に新しくブランチを作成してpush
5. Github上でpull requestを送る
6. 管理者がレビューする
7. 問題があれば差し戻す
8. 再度問題を確認し、`add`, `commit`, `push`で修正内容をpull reqに上乗せして送る
    + pull req中に同じブランチに修正内容をpushすると修正内容がPull reqに乗っかる
9. 修正内容を確認し、mergeする
10. ブランチを削除する

### ブランチの切り替え方
+ `git checkout ブランチ名`コマンドでブランチを行き来できる
    + 現在いるランチ上で何かしたらの変更を行っていた場合はその変更内容を保存もしくは削除してからブランチを切移動すること

### commitコメントの修正
+ `git commit --amend -m "新規コメント"` コマンドで編集可能

### 指定したコミットまでコードを遡る方法
1. Github上（もしくはlog上）でコミットのハッシュをコピー
2. `git checkout ハッシュ` コマンドで指定したコミットまで戻る
3. `git checkout ブランチ名` コマンドで最新のコミットに戻る
