# [진료 순서 정하기](https://school.programmers.co.kr/learn/courses/30/lessons/120835)
```java
import java.util.Arrays;

class Solution {
    public int[] solution(int[] emergency) {

        int[] originalArr = Arrays.copyOfRange(emergency, 0, emergency.length);
        int[] answer = new int[emergency.length];

        Arrays.sort(emergency);

        for(int i = 0; i < originalArr.length; i++) {
            for(int j = 0; j < emergency.length; j++) {
                if(originalArr[i] == emergency[j]) {
                    answer[i] = emergency.length - j;
                }
            }
        }

        return answer;
    }
}
```

- 알게된 점
1. 풀어 본 문제인데도 어려웠다.
2. 배열의 sort() 함수는 변수에 저장되지 않는다.