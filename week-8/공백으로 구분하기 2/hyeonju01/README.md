[공백으로 구분하기 2](https://school.programmers.co.kr/learn/courses/30/lessons/181868)
```java
import java.util.*;

class Solution {
    public String[] solution(String my_string) {
        String[] splitted = my_string.split(" ");
        ArrayList<String> list = new ArrayList<>();
        for (String a: splitted) {
            if (!a.equals("")) {
                list.add(a);
            }
        }
        return list.stream().toArray(String[]::new);
    }
}
```