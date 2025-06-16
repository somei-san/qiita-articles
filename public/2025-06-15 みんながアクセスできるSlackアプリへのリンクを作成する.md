---
title: みんながアクセスできるSlackアプリへのリンクを作成する
tags:
  - tips
  - Slack
private: false
updated_at: '2025-06-15T11:37:44+09:00'
id: 99c4776423900c6aff6c
organization_url_name: null
slide: false
ignorePublish: false
---

## 背景

右クリックから取得できるSlackアプリへのリンクは各ユーザー固有のものになっており、他のユーザーがクリックしても該当するアプリに飛べない
これだとワークフローなどで仕組み化するときに不便なので、みんながアクセスできるSlackアプリへのリンクを作りたい

## 結論

Deep Link を作成すればいい

## どうするか？

Deep Link は次のような構成になっている

```
slack://app?team={TEAM_ID}&id={APP_ID}
```

__TEAM_ID__ はワークスペースの識別子で、Slack URL の冒頭部分から確認できる

例： `https://sample-workspace.slack.com/`
→ `sample-workspace`

__APP_ID__ はアプリの識別子で、Slackアプリの Marketplace URL から確認できる

例: `https://sample-workspace.slack.com/marketplace/B05XYZH4XGX--sample-app`
→ `B05XYZH4XGX`

上記の例に基づくと、以下のようになる

```
slack://app?team=sample-workspace&id=B05XYZH4XGX
```

## 補足

実は `@App名` でメンションできちゃうので、メッセージで共有する場合には別に Deep Link いらない
