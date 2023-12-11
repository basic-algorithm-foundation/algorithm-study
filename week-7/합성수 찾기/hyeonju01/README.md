# [합성수 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/120846)
```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        for(int i = 1; i < n + 1; i++) {
            int num = 0;
            for (int j = 1; j <= i; j++) {
                if (i % j == 0) {
                    num ++;
                }
            }
            if (num > 2) {
                answer ++;
            }
        }
        return answer;  
    }
    
}
```

- 알게된 점
  약수 개수를 찾는 반복문의 스코프에서 num을 선언했더니 1 이상으로 누적되지 않았다. 기본기를 잘 챙기자.
