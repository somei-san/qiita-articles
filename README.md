# Qiitaの記事です

- [アカウントのHome](https://qiita.com/goyaYellow)
- [このRepository](https://github.com/somei-san/qiita-articles)

# 設定

## GithubActionsによる自動Publish

[actionsファイル](.github/workflows/publish.yml)

### publish条件

- `./public`配下に差分があったらCIが回ります
- Front Matterの`ignorePublish`が`false`ならpublish対象になります（デフォルト`false`）
- Qiita側の記事と差分がなければpublishされません

### publish時の備忘

- Front Matterの`title`の値が記事名になります. ファイル名ではありません.

# 個人的備忘

## 新しく記事を書き始める

```shell
npx qiita new 記事のファイルのベース名
```

## プレビューする

```shell
npx qiita preview
```

## 画像の上げ方

[これを参照](https://qiita.com/ak-sakatoku/items/3e429643500e2d0585bf#:~:text=%E3%83%AD%E3%83%BC%E3%83%89%E3%81%A7%E3%81%8D%E3%81%AA%E3%81%84-,%E7%94%BB%E5%83%8F%E3%81%AE%E3%82%A2%E3%83%83%E3%83%97%E3%83%AD%E3%83%BC%E3%83%89%E3%81%AF%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%99%EF%BC%81,-%E3%83%97%E3%83%AC%E3%83%93%E3%83%A5%E3%83%BC%E3%81%AB%E3%82%82)

# 参考

- [Qiita CLI README](https://github.com/increments/qiita-cli/blob/main/README.md#github-%E3%81%A7%E8%A8%98%E4%BA%8B%E3%82%92%E7%AE%A1%E7%90%86%E3%81%99%E3%82%8B)
- [Front Matterの解説](https://github.com/increments/qiita-cli/blob/main/README.md#Qiita-CLI-%E3%81%A7%E8%A8%98%E4%BA%8B%E3%82%92%E7%AE%A1%E7%90%86%E3%81%99%E3%82%8B)
