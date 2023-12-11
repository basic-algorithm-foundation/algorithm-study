[n 번째 원소부터](https://school.programmers.co.kr/learn/courses/30/lessons/181892)
```java
import java.util.Arrays;

class Solution {
    public int[] solution(int[] num_list, int n) {
        int numLen = num_list.length; 
        return Arrays.copyOfRange(num_list, n-1, numLen);
    }
}
```