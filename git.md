# Git Cheat Sheet & Tips

### リポジトリの作成
`git init`

---

### リモートリポジトリの設定
`git remote add [username] [remote repository path]`

---

### ステージング(インデックス)への追加
- ファイル指定<br/>
`git add [file path]`
- 変更のある全ファイル<br/>
`git add -A`

---

### コミット
`git commit -m "commit message"`

- 直前のコミットの変更<br/>
`git commit --amend`

---

### コミットの取り消し
- 現在のブランチの一つ前のコミットに戻す（最新コミットを無かったことにする）
`git reset --hard HEAD~`

- リセットのパターン

| モード名    | HEADの位置   | インデックス   | ワークツリー   |
|:-----------|:----------- |:-------------|:------------|
| soft       | 変更する     | 変更しない     | 変更しない    |
| mixed      | 変更する     | 変更する       | 変更しない    |
| hard       | 変更する     | 変更する       | 変更する      |

---

### プッシュ
- 初回<br/>
`git push -U [remote name] [remote branch name]`
- 二回目以降<br/>
`git push [remote name]`

---

### ブランチ操作
- 新規ブランチ作成<br/>
`git branch [branch name]`

- 全ブランチ一覧の表示<br/>
`git branch -a`

- ブランチの切り替え<br/>
`git checkout [branch name]`

- ブランチの削除<br/>
`git branch -d [branch name]`

- ブランチ名の変更
`git branch -m [branch name] [new branch name]`
---

### コミットログの表示
- リスト表示
`git log`

- グラフ表示
`git log --graph`

- 全ブランチ表示
`git --all`

- 変更ファイル名の表示
`git --name-status`

- ブランチ名とHEADの表示
`git --decorate=full`

- ベストチョイス
`git log --all --name-status --graph --oneline --decorate=full`

---

### diff(差分確認)
- 最終コミットとの比較<br/>
`git diff HEAD^`

- コミット同士の比較<br/>
`git diff [commit id1(hash)] [commit id2(hash)]`

---

### リポジトリとワークスペースの差分ファイルの抽出
`git status`

---

### コミット内容の確認
- 最新コミットの内容確認<br/>
`git show`

- コミット指定で内容確認<br/>
`git show [commit id(hash)]`

---

### リバート（逆コミット）
`git revert [commit id(hash)]`

---

### プル

`git pull [remote repository PATH] [branch name]`

---

### マージ

- 現在のブランチへ他のブランチをマージする<br/>
`git merge [branch name]`

---

### tag

- タグの一覧表示<br/>
`git tag`

- 注釈を含めてタグ一覧表示<br/>
`git tag -n`

- タグの作成<br/>
`git tag -am ["comment"] [tag_name]`

- タグの削除<br/>
`git tag -d [tag_name]`
---

### stash

- 現状の保存<br/>
`git stash`

- 保存リストの表示<br/>
`git stash list`

- 復元<br/>
`git stash pop stash@{[number]}`
---

### cherry-pick
`git cherry-pick [commit id(hash)]`

---

### 設定関連
- リポジトリの設定表示<br/>
`git config -l`

- ユーザ名の設定<br/>
`git config --global user.name [username]`

- ユーザメールアドレスの設定<br/>
`git config --global user.email [email address]`

---
