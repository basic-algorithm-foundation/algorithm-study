# [순서쌍의 개수](https://school.programmers.co.kr/learn/courses/30/lessons/120836)
```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        for(int i = 1; i < n+1; i++) {
            if (n % i == 0) {
                answer ++;
            }
        }
        return answer;
    }
}
```

- 알게된 점
1. n이 100만인데 돌아가는데, 풀기 전에는 돌아갈 지 몰랐다. 시간복잡도 구하는 법 공부해야겠다.