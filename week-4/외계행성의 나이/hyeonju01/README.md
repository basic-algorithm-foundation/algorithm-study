# [외계행성의 나이](https://school.programmers.co.kr/learn/courses/30/lessons/120834)
```java
import java.util.Map;

class Solution {
    public String solution(int age) {
        String answer = "";
        String ageStr = Integer.toString(age);
        Map<String, String> dictionary = Map.of(
            "0", "a",
            "1", "b",
            "2", "c",
            "3", "d",
            "4", "e",
            "5", "f",
            "6", "g",
            "7", "h",
            "8", "i",
            "9", "j" );

        for(int i = 0; i < ageStr.length(); i++) {
            char c = ageStr.charAt(i);
            answer = answer.concat(
                dictionary.get(Character.toString(c)));
        }

        return answer;
    }
}
```

- 알게된 점
1. Map, Set의 쓰임과 메서드에 익숙해져야겠다.