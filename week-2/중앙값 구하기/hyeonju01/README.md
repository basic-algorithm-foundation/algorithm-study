# [중앙값 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/120811)
```java
import java.util.Arrays;

class Solution {
    public int solution(int[] array) {
        int answer = 0;
        Arrays.sort(array);
        int midIdx = (array.length - 1) / 2;
        return array[midIdx];
    }
}
```

- 알게된 점
1. 풀어본 문제인데, 배열 정렬할 때 sort를 사용하지 않는 방법이 전혀 기억이 안난다. 정렬 구현 문제 연습해봐야겠다.