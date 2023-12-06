# [구슬을 나누는 경우의 수](https://school.programmers.co.kr/learn/courses/30/lessons/120840)
### ❌ 틀린 답
```java
class Solution {
    public int solution(int balls, int share) {
        
        return permutation(balls, share) / factorial(share);
    }
    
    public int factorial(int n) {
        if (n == 1) {
            return 1;
        } else {
            return n * factorial(n-1);
        }
    }
    
    public int permutation(int n, int r) {
        
        if (r == 0) {
            return 1;
        } else {
            return n * permutation(n-1, r-1);
        }
        
    }
}
```
- 테스트 케이스 통과, 정확성 테스트 54.3/100

### 🗒️ 풀이 참고
```java
class Solution {
    public int solution(int balls, int share) {
        Long answer = 1L; // balls = 30, share 5
        int cnt = 1;
        while(cnt <= share) {
            answer = answer * balls; 
            // 1L * 30, (1L*30 / 1) * 29, (((1L*30 / 1) * 29) / 2) * 28, 
            balls --; // 29, 28, 27
            answer = answer / cnt; 
            // 1L*30 / 1, ((1L*30 / 1) * 29) / 2, ((((1L*30 / 1) * 29) / 2) * 28)/3
            cnt ++; // 2, 3, 4
            
        }
        
        return answer.intValue();
    }
}
```

- 알게된 점
1. 힌트에 나온 공식을 단순화하여 이를 반복문으로 구현한 풀이를 참고했다.
2. intValue() 메서드는 Long 타입 객체에 바로 사용할 수 있다.