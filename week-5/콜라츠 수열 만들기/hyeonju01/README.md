# [콜라츠 수열 만들기](https://school.programmers.co.kr/learn/courses/30/lessons/181919)
```java
import java.util.List;
import java.util.ArrayList;

class Solution {
    public int[] solution(int n) {
        int[] answer = {};
        List<Integer> list = new ArrayList<>();
        while(n >= 1) {
            if (n % 2 == 0) { // 짝수
                list.add(n);
                if (n!= 1 ) {
                    n /= 2;
                } else {
                    break;
                }
            } else { // 홀수
                list.add(n);
                if (n!= 1) {
                    n = (3 * n) + 1;
                } else {
                    break;
                }
            }
        }
        return list.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

- 알게된 점
if, else문을 사용하지 않는 방법으로 리팩토링 해봐야겠다.