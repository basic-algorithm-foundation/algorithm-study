[배열의 원소만큼 추가하기](https://school.programmers.co.kr/learn/courses/30/lessons/181861)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(int[] arr) {
        int arrLen = arr.length;
        ArrayList<Integer> list = new ArrayList<>();
        for(int i = 0; i < arrLen; i++) {
            int num = arr[i];
            for (int j = 0; j < num; j++) {
                list.add(num);
            }
        }

        return list.stream().mapToInt(Integer::intValue).toArray();
    }
}
```