---
title: GitHubで、自分にレビュー依頼されている & 自分がレビュー済み & まだOpen、なプルリク一覧をみる
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

GitHubデフォルトの[Review Request](https://github.com/pulls?q=is%3Aopen+is%3Apr+review-requested%3A%40me+archived%3Afalse+)では、レビューをしちゃうと消えちゃって確認できなくなるので



