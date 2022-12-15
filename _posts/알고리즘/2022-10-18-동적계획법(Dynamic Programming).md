---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_What_is_this
title: "동적계획법"

# post specific
# if not specified, .name will be used from _data/owner.yml
author: 공지혁
# multiple category is not supported
category: Algorithm
# multiple tag entries are possible
tags: [Algorithm]
# thumbnail image for post
img: "https://blog.kakaocdn.net/dn/xCxbD/btq3zN4NQ3x/0ZBXlRgaeTqT1hBmPBrOQk/img.png"
# disable comments on this page
#comments_disable: true

# publish date
date: 2022-10-18 10:04:30 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-11-25 10:04:30 +0900
# check the meta_common_description in _data/lang/[language].yml
#meta_description: ""

# optional
# if you enabled image_viewer_posts you don't need to enable this. This is only if image_viewer_posts = false
#image_viewer_on: true
# if you enabled image_lazy_loader_posts you don't need to enable this. This is only if image_lazy_loader_posts = false
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---

# 동적계획법 (Dynamin Programming)
DP(동적계획법)는 **하나의 큰 문제를 여러 개의 작은 문제로 나누어 그 결과를 저장하여 다시 큰 문제를 해결할 때 사용**하는 것을 말한다.

## Dynamic Programming의 조건
- 작은 문제가 반복이 일어나는 경우.

- 같은 문제는 구할 때마다 정답이 같다.

위 와같은 조건을 만족하는 경우에만 동적프로그래밍을 사용할 수 있다. 작은 문제의 결과 값이 항상 같다는 점을 이용해서 큰문제를 해결하는 방법.

## 메모이제이션(Memoization)
메모이제이션은 동적프로그래밍에서는 작은 문제들이 반복되고 이 작은 문제들의 결과값이 항상 같다. 때문에 이점을 이용하여 한번 계산한 작은 문제를 저장해놓고 다시 사용을 한다. 이것을 Memoization이라고 한다.

동적계획법에서 간단한 예시로는 피보나치가 있다.
피보나치는 **다음수열 = 이전 수열 + 두 단계 전 수열**이라는 점화식을 가지고 있다. 재귀 함수로 풀게되면 이보다도 훨씬 간단하게 풀 수 있지만 n이 증가함에 따라 호출되는 함수의 수가 기하급수적으로 증가하기 때문에 일정 수 이상의 순열을 구하기가 어렵다.

``` python
def memoization_fibo(n):
    dp[0] = 1
    dp[1] = 1
​
    if n < 2:
        return dp[n]
​
    for i in range(2, n+1):
        dp[i] = dp[i-2] + dp[i-1]
​
    return dp[n]
​
```
동적계획법을 이용해서 푼 코드이다. 0, 1번째 수열은 항상 1이고, 그 다음 수열은 점화식을 배열에 미리 저장하여 다음 수를 계산할때 계산을 줄일수 있다.
