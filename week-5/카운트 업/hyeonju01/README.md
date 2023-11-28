# [카운트 업](https://school.programmers.co.kr/learn/courses/30/lessons/181920)
```java
import java.util.ArrayList;
import java.util.List;

class Solution {
    public int[] solution(int start_num, int end_num) {
        List<Integer> list = new ArrayList<>();
        for(int i = start_num; i < end_num + 1; i++) {
            list.add(i);
        }
        return list.stream().mapToInt(Integer::intValue).toArray();
    }
}
```