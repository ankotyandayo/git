githubでとりあえず覚えておけばいいやつまとめた

１まず、github側(remote)でリポジトリを作る

２git init  localでもデータの保管場所をつくる　ls -aで見れるよ

３git add README.md 作成したファイルを一時保存する　git add -A .ですべてを追加

４git commit -m "" セーブポイントとしてまとめる

５git branch -M main　 ブランチ名を変更

６git remote add origin リポジトリのurl (どこのremoteリポジトリ追加するか指定する)

７git push origin main　※git push -u origin main　(-u → --set-upstream　次回からgit pushだけでよくなる) ★originというは現在のlocal側の話 mainはremoteのブランチ名

originは共通でいいけど、remoteのブランチ名はlocalのブランチを変えたときは変えないとエラー

2回目以降のpushは３、４、７だけでいい

branchについて
branchはゲームのセーブデータのようなもん(分けれる)

１git branch ブランチ名　　ブランチを作成する
　git checkout -b ブランチ名　　↑と同様にブランチを作成する
★git switch -c ブランチ名　　　↑と同様にブランチを作成するかつ、ブランチを切り替える　これを使うべき

２git checkout ブランチ名　　ブランチを切り替える
　git switch ブランチ名

３git branch ローカル側のブランチの一覧を見れる
　git branch -a リモートを含めたブランチの一覧を見れる

切り分けたブランチをくっつける方法
github側で　compare&pullrequestを押す


・git status
前回のcommitからの差分を見れる

・git --amend -m "修正されたコミットメッセージ"
git commitをしなおしたいときに使う
もう一度git addをして、git --amendをすれば、前回のgit commitを取り消してくれる

★git --amend --no-editこれを使えば前回のメッセージをそのまま使える

・git log --oneline コミットをしたログを見れる



git pull リモートの内容を読み込む

詳しくはhttps://qiita.com/2m1tsu3/items/6d49374230afab251337
この記事にまとまっている
