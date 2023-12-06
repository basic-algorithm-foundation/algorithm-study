# [접미사 배열](https://school.programmers.co.kr/learn/courses/30/lessons/181909)
```java
import java.util.ArrayList;

class Solution {
    public String[] solution(String my_string) {
        ArrayList<String> list = new ArrayList<>();
        int s = 0;
        int e = my_string.length();
        for(int i = 0; i < my_string.length(); i++) {
            list.add(my_string.substring(s, e));
            s ++;
        }
        return list.stream().sorted().toArray(String[]::new);
    }
}
```

- 라이브러리 Import 시 생성자 괄호 사용하지 않도록 주의해서 런타임 에러 떴다. 주의할 것.