# [공 던지기](https://school.programmers.co.kr/learn/courses/30/lessons/120843)
```java
class Solution {
    public int solution(int[] numbers, int k) {
        int answer = 0; // 순서
        int shooter = 0; // 공던지는 사람
        int idx = 0; // 인덱스
        
        while (true) {
            if (idx < numbers.length) {
                shooter = numbers[idx];
                idx += 2;
                answer ++; // 2
            } else if (idx >= numbers.length) {
                idx %= numbers.length;
                shooter = numbers[idx];
                idx += 2;
                answer ++;
            }
            
            if (answer == k) {
                break;
            } else {
                continue;
            }
        }
        
        return shooter;
    }
}
```

- 알게된 점
코드가 생각한 로직대로 작동하지 않는 이유는 빼먹은 코드가 있어서임을 명심하자
