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

### issuesを使ってみよう
1. issuesの作成
- issuesは、リポジトリごとに管理されます
- リポジトリのトップページから[Issues]タブを選択し、[New issue]をクリックする

![image](https://user-images.githubusercontent.com/41432482/155464030-4b0ac63d-adf7-4d77-ac6a-7909f574ca91.png)
![image](https://user-images.githubusercontent.com/41432482/155464051-17876d7e-f313-4948-90f9-cd43bb48d5e3.png)

2. issueのタイトルや内容を記述する
- タイトルは一目である程度内容がわかるものにする
- 内容はMarkdown記法で記述する

![image](https://user-images.githubusercontent.com/41432482/155465149-a66e8576-2457-4ab5-9af6-c36cc2c5b752.png)


3. issueの担当者を決める

![image](https://user-images.githubusercontent.com/41432482/155465400-eeed0b79-8a84-4053-82bc-002670f464d2.png)


4. issueを閉じる

![image](https://user-images.githubusercontent.com/41432482/155465611-61c9446c-296d-4949-b91a-b707b76c296b.png)
![image](https://user-images.githubusercontent.com/41432482/155465706-e7518580-3b47-46ea-ad49-f2914dfdaf0e.png)
![image](https://user-images.githubusercontent.com/41432482/155465763-fea86f4e-3f55-4df0-b2a8-25473d9e02d5.png)

