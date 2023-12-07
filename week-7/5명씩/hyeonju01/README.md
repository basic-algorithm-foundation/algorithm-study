# [5명씩](https://school.programmers.co.kr/learn/courses/30/lessons/181886)
```java
import java.util.ArrayList;

class Solution {
    public String[] solution(String[] names) {
        ArrayList<String> list = new ArrayList<>();
        int wholePeopleNum = names.length;

        for(int i = 0; i < wholePeopleNum; i+= 5) {
            list.add(names[i]);
        }

        return list.stream().toArray(String[]::new);
    }
}
```