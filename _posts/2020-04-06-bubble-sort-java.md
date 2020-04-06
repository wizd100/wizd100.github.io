---
layout: post
title:  "거품정렬(버블정렬 bubble sort) java 소스코드"
permalink: /:categories/:year/:month/:day/:title/
date:   2020-04-06 16:30:00 +0900
categories: posts
tags: [정렬, 알고리즘, java]
use_math: true
---

<iframe width="100%" height="500" src="https://www.youtube.com/embed/lyZQPjUT5B4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 버블정렬의 특징
- 장점
    - 구현이 간단함
- 단점
    - 다른 정렬에 비해 속도가 느림 

## 시간복잡도
- 최악 시간복잡도 : $$O(n^2)$$ 비교, $$O(n^2)$$ 교환
- 최선 시간복잡도 : $$O(n)$$ 비교, $$O(1)$$ 교환
- 평균 시간복잡도 : $$O(n^2)$$ 비교, $$O(n^2)$$ 교환


## java 소스 구현

```java
public class Bubble {
    public static void main(String[] args) {
        int[] arr = {30, 5, 21, 10, 4, 13, 8, 25, 19, 1};
        
        //-i를 하는 이유? -> 제일 큰수가 맨 마지막으로 정렬이 됨 (맨 마지막은 비교를 안해도 된다는 것)
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        //1 4 5 8 10 13 19 21 25 30
        for (int i = 0; i < arr.length; i++) {
            System.out.printf("%d ", arr[i]);
        }
    }
}
```


