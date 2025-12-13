---
title: GitHubで、自分がレビュアー&レビュー済み&まだOpen、なプルリク一覧を確認する
tags:
  - GitHub
  - tips
private: false
updated_at: '2025-06-16T13:02:17+09:00'
id: 486bc4ffe9467a01ad36
organization_url_name: null
slide: false
ignorePublish: false
---
## 結論

```
is:open is:pr reviewed-by:@me -author:@me 
```

でフィルタをかける

[URL化したもの](https://github.com/pulls?q=is%3Aopen+is%3Apr+reviewed-by%3A%40me+-author%3A%40me)

# 背景

GitHubデフォルトの[Review Request](https://github.com/pulls/review-requested)では、レビューをしちゃうと消えちゃって確認できなくなるので



