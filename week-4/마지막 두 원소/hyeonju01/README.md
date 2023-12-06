# [마지막 두 원소](https://school.programmers.co.kr/learn/courses/30/lessons/181927)
```java
import java.util.*;

class Solution {
    public int[] solution(int[] num_list) {
        int[] answer;
        List<Integer> answerList = new ArrayList<>();
        for (int num: num_list) {
            answerList.add(num);
        }

        int lastIdx = num_list.length - 1;
        int lastNum = 0;

        if (num_list[lastIdx] > num_list[lastIdx - 1]) {
            lastNum = num_list[lastIdx] - num_list[lastIdx - 1];
            answerList.add(lastNum);
        } else {
            lastNum = num_list[lastIdx] * 2;
            answerList.add(lastNum);
        }

        answer = answerList.stream().mapToInt(Integer::intValue).toArray();

        return answer;
    }
}
```