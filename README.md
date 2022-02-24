# Git授業用
R4年　モリジョビ　授業用

## READMEの作成
- READMEとはよくある「使用前にお読みください」というやつです。
- GitHubでは公開しているソフトウェアの使い方を記述している事が多いです。
- GitHubのREADMEはMarkDownで記述します。（書き方は[こちら](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)）

## リポジトリをcloneする
- 'clone'とはGitHubに公開されているリポジトリをローカルリポジトリに複製する機能です。
- 'clone'は'https方式'または'SSH方式'のどちらかで行う(今回はSSHで行います)

![image](https://user-images.githubusercontent.com/41432482/155455325-710be119-81bf-459f-a500-bb9a70f6283a.png)

```
git clone git@github.com:otsubo-jyobi/Git-class.git
```

## ローカルの変更をGitHubに反映させる
1. cloneしたフォルダに'sample.txt'を作成する
2. 作成した'sample.txt'にデータを書き込む

```
echo "hogehoge" > sample.txt
```

3. ステージングした後、コミットする
4. ローカルリポジトリの変更をGitHubリポジトリに反映させる

```
git push origin main
```

※SSH-key設定をする必要あり

## GitHubの状態をリモートリポジトリに反映させる
1. GitHubの状態をリモートリポジトリに反映させる

```
git pull origin main
```

## branchを使ってみよう
1. fixブランチを作成する

```
git branch fix
```

2. mainブランチからfixブランチに切り替える 

```
git switch fix
```

3. fixブランチでファイルに変更を加え、コミットする

```
echo "fugafuga" >> sample.txt
git add sample.txt
git commit -m "add sample.txt"
```

4. Githubにプッシュし、状態を確認してみるとfixブランチが追加されていることが確認できる

```
git push origin fix
```

![image](https://user-images.githubusercontent.com/41432482/155455054-ab0e5272-74fb-471d-8bb6-f6efef202c96.png)

5. ブランチをマージしてみよう
- ブランチをのマージを依頼することを「pull request」という

![image](https://user-images.githubusercontent.com/41432482/155456621-cf672164-fe7e-4716-a6d6-2437ec7bab46.png)
　
6. fixブランチの内容がmainブランチに反映されている事を確認する

## コンフリクトを体験
1. コンフリクトを発生させる
2. コンフリクトを解消させる

## チーム開発の準備をしてみよう
- 共同開発を行うには２つの方法があります。リポジトリを共有する方法と、forkで行う方法です。

### リポジトリの共有
1. コラボレーターに他のメンバーを登録する

### forkを使ってみる
1. リポジトリをforkする

