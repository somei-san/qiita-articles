---
title: GitHubで、自分がレビュアー&レビュー済み&まだOpen、なプルリク一覧を確認する
tags:
  - 'tips'
  - 'GitHub'
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: true
---
## 結論

```
is:open is:pr reviewed-by:@me -author:@me 
```

でフィルタをかける

[URL化したもの](https://github.com/pulls?q=is%3Aopen+is%3Apr+reviewed-by%3A%40me+-author%3A%40me)

# 背景

GitHubデフォルトの[Review Request](https://github.com/pulls/review-requested)では、レビューをしちゃうと消えちゃって確認できなくなるので



