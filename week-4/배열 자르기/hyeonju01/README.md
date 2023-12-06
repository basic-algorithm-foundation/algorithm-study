# [배열 자르기](https://school.programmers.co.kr/learn/courses/30/lessons/120833)
```java
class Solution {
    public int[] solution(int[] numbers, int num1, int num2) {
        int[] answer = new int[num2 - num1 + 1];

        int idx = 0;

        for(int i = 0; i < numbers.length; i++) {
            if(i >= num1 && i <= num2) {
                answer[idx] = numbers[i];
                idx ++;
            }

        }

        return answer;
    }
}
```

- 알게된 점
1. **Arrays.copyOfRange** 함수 사용법 익혀두자.