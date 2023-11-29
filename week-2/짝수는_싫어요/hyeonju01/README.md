# [짝수는 싫어요](https://school.programmers.co.kr/learn/courses/30/lessons/120813)
```java
import java.util.*;

class Solution {
    public int[] solution(int n) {
        List<Integer> answer = new ArrayList<>();

        for(int i = 1; i <= n; i+=2) {
            answer.add(i);
        }

        return answer.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

- 알게된 점
1. stream() : 주어진 ArrayList를 stream으로 변환한다.
2. mapToInt() : stream을 IntStream으로 변환한다.
3. toArray(): array로 반환한다. 
4. ```Integer::intValue```
   - Methor Reference(메서드 참조)
   - Integer 클래스의 intValue 메소드는 Integer 객체를 int type으로 변환하는데, 메서드 참조를 통해 코드를 간결하게 나타낼 수 있다.
   - 자바 8 이상부터 추가된 스트림 API를 사용한 패턴!