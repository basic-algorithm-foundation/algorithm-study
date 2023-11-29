# [배열 만들기 4](https://school.programmers.co.kr/learn/courses/30/lessons/181918)
```java
import java.util.List;
import java.util.ArrayList;

class Solution {
    public int[] solution(int[] arr) {
        List<Integer> stk = new ArrayList<>();
        
        int idx = 0;
        int stkSize;
        
        while(idx < arr.length) {
            stkSize = stk.size();
            if (stk.isEmpty()) {
                stk.add(arr[idx]);
                idx++;
            } else if (!stk.isEmpty() &&
                     stk.get(stkSize - 1) < arr[idx]) {
                stk.add(arr[idx]);
                idx ++;
            } else if(!stk.isEmpty() &&
                     stk.get(stkSize - 1) >= arr[idx]) {
                stk.remove(stkSize - 1);
            }
        }
        return stk.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

- 알게된 점
1. idx를 다루는 변수의 경우, 초깃값에서 -1을 할 경우 인덱스 예외가 발생할 수 있으니, size를 구해 놓고 사용될 때 -1을 해야 한다.