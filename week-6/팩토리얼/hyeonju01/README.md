# [팩토리얼](https://school.programmers.co.kr/learn/courses/30/lessons/120848)

### 오답
```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        // n!
        for(int i = 1; i <= n; i++) {
            if (factorial(i) < n) {
                answer = i;
                continue;
            } 
        }
        return answer;
    }
    
    public int factorial(int n) {
        if (n == 1) {
            return 1;
        } else {
            return n * factorial(n - 1);
        }
    }
}
```
- 재귀를 사용하면 n의 최댓값(3628800)에서 시간 초과

```java
    static class Solution {
        public int solution(int n) {
            int answer = 0;
            int temp = 1;
            int i = 1;
            while(true) {
                answer = i;
                temp = temp * i; // get factorial
                if (temp >= n) {
                    break;
                } else {
                    i++;
                }
            }
            return answer;
        }
}
```
- n과 i!이 같을 경우, n보다 i!이 큰 경우를 나누지 않아서 틀림

### 정답
```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        int temp = 1;
        int idx = 1;
        
        while(true) {
            answer = idx;
            temp = temp * idx; // get factorial
            if (temp > n) {
                answer = idx-1;
                break;
            } else if (temp == n){
                break;
            } else {
                idx++;
            }
        }
        
        return answer;
    }
}
```

- 알게된 점
1부터 2, 3, ..., n까지 곱한 후 비교하는 방식을 사용함
