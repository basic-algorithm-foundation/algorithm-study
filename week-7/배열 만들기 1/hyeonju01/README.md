# [배열 만들기 1](https://school.programmers.co.kr/learn/courses/30/lessons/181901)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(int n, int k) {
        ArrayList<Integer> answer = new ArrayList<>();
        // 범위: 1 ~ n, 그 중 k의 배수를 오름차순으로 저장 

        for(int i = 1; i < n+1; i++) {
            if ((i % k) == 0) {
                answer.add(i);
            }
        }

        return answer.stream().sorted().mapToInt(Integer::intValue).toArray();
    }
}
```