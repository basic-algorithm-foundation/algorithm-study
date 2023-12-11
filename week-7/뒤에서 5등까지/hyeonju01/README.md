[뒤에서 5등까지](https://school.programmers.co.kr/learn/courses/30/lessons/181853)
```java
import java.util.Arrays;

class Solution {
    public int[] solution(int[] num_list) {
        int[] answer = {};
        Arrays.sort(num_list);
        
        return Arrays.copyOfRange(num_list, 0, 5);
    }
}
```