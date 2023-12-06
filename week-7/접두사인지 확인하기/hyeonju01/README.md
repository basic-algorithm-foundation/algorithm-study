# [접두사인지 확인하기](https://school.programmers.co.kr/learn/courses/30/lessons/181906)
```java
import java.util.ArrayList;

class Solution {
    public int solution(String my_string, String is_prefix) {
        // int answer = 0;
        ArrayList<String> prefixes = new ArrayList<>();

        int s = 0;
        
        for(int e = 1; e < my_string.length(); e++) {
            prefixes.add(my_string.substring(s, e));
        }
        
        String[] prefixesArr = prefixes.stream().toArray(String[]::new);
        
        for(String prefix: prefixesArr) {
            if (prefix.equals(is_prefix)) {
                return 1;
            }
        }
        
        return 0;
    }
}
```

- 실행 결과, 최대 런타임(20.39ms), 최소 런타임(1.21ms)이 차이 나는 이유가 궁금하다. 로직 개선과 함께 생각해봐야겠다.