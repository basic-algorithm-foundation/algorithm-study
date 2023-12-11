[정수 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/181840)

```java
import java.util.Arrays;

class Solution {
    public int solution(int[] num_list, int n) {
        List<Integer> list = IntStream.of(num_list).boxed().collect(Collectors.toList());

        return list.contains(n) ? 1: 0;
    }
}
```