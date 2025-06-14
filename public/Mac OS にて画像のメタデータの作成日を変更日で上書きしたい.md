---
title: Mac OS にて画像のメタデータの作成日を変更日で上書きしたい
tags:
  - Mac
  - tips
private: false
updated_at: '2025-06-14T21:55:50+09:00'
id: 4d70e5599e196c4eb608
organization_url_name: null
slide: false
ignorePublish: false
---

## 背景
iOS 上での表示順は作成日に準拠するが、DropBox などを経由して Mac に保存すると同期日が作成日になり、順番がめちゃくちゃになるのをどうにかしたい


## 手順

### ExifTool をインストールする

```sh
brew install exiftool
```

### 画像の置いてあるディレクトリで以下のコマンドを実行する
```sh
exiftool '-DateTimeOriginal<FileModifyDate' '-CreateDate<FileModifyDate' -r -overwrite_original -P -m .
```

## オプション解説
- `-DateTimeOriginal<FileModifyDate`： ファイルの変更日を元に写真の撮影日を設定する
-  `-CreateDate<FileModifyDate`： ファイルの変更日を元に画像の作成日を設定する
- `-r`： 再帰的にフォルダ内の全ファイルを処理します
- `-overwrite_original`： 元ファイルを上書きし、バックアップファイルを作成する
- `-P`： ファイルの更新日（変更日）を変更しないようにする
- `-m`： 軽微な警告（minor warning）が表示されないようにする

## メモ
mp4, mov にも有効だった
