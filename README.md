# Qiita の記事

- [アカウント Home](https://qiita.com/goyaYellow)
- [この Repository](https://github.com/somei-san/qiita-articles)

# 設定

## GithubActionsによる自動Publish

[actionsファイル](.github/workflows/publish.yml)

### publish条件

- `./public`配下に差分があったらCIが回ります
- Front Matterの`ignorePublish`が`false`ならpublish対象になります
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

# 参考

- [Qiita CLI README](https://github.com/increments/qiita-cli/blob/main/README.md#github-%E3%81%A7%E8%A8%98%E4%BA%8B%E3%82%92%E7%AE%A1%E7%90%86%E3%81%99%E3%82%8B)
- [Front Matterの解説](https://github.com/increments/qiita-cli/blob/main/README.md#Qiita-CLI-%E3%81%A7%E8%A8%98%E4%BA%8B%E3%82%92%E7%AE%A1%E7%90%86%E3%81%99%E3%82%8B)
