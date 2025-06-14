---
title: Mac OS にて画像のメタデータの作成日を変更日で上書きしたい
tags:
  - ''
private: false # true: 限定共有記事 / false: 公開記事
updated_at: '' # 記事を投稿した際に自動的に記事の更新日時に変わります
id: null # 記事を投稿した際に自動的に記事のUUIDに変わります
organization_url_name: null # 関連付けるOrganizationのURL名
slide: false # true: スライドモードON / false: スライドモードOFF
ignorePublish: true # true: `publish`コマンドにおいて無視されます（Qiitaに投稿されません） / false: `publish` コマンドで処理されます（Qiitaに投稿されます）
---

# 背景
ios 上での表示順は作成日に準拠するが、DropBoxなどを経由して Mac に保存すると同期日が作成日になり、順番がめちゃくちゃになるのをどうにかしたい


# 結論
画像のおいてあるディレクトリで以下のコマンドを実行する
```shell
exiftool '-DateTimeOriginal<FileModifyDate' '-CreateDate<FileModifyDate' -r -overwrite_original -P -m .
```

# オプション解説
 • `-DateTimeOriginal<FileModifyDate`： ファイルの変更日を元に写真の撮影日を設定します。
 • `-CreateDate<FileModifyDate`： ファイルの変更日を元に画像の作成日を設定します。
 • `-r`： 再帰的にフォルダ内の全ファイルを処理します。
 • `-overwrite_original`： 元ファイルを上書きし、バックアップファイルを作成しない。
 • `-P`： ファイルの更新日（変更日）を変更しないようにします。
 • `-m`： 軽微な警告（minor warning）が表示されないようにする

# メモ
mp4, mov にも有効だった