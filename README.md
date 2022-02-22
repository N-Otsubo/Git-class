# Git授業用
R4年　モリジョビ　授業用

## READMEの作成
- READMEとはよくある「使用前にお読みください」というやつです。
- GitHubでは公開しているソフトウェアの使い方を記述している事が多いです。
- GitHubのREADMEはMarkDownで記述します。（書き方は[こちら](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)）

## リポジトリをcloneする
- 'clone'とはGitHubに公開されているリポジトリをローカルリポジトリに複製する機能です。
- 'clone'は'https方式'または'SSH方式'のどちらかで行う

```
git clone [ http-URL or SSH-URL ]
```

## ローカルからの変更をGitHubに反映させる
1. cloneしたフォルダに'sample.txt'を作成する
2. 作成した'sample.txt'にデータを書き込む

```echo "hogehoge" > sample.txt```

3. ステージングした後、コミットする
4. ローカルリポジトリの変更をGitHubリポジトリに反映させる

```git push origin main```

6. 
