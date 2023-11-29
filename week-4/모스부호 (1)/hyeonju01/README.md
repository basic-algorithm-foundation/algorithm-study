# [모스부호 (1)](https://school.programmers.co.kr/learn/courses/30/lessons/120838)
```java
import java.util.*;

class Solution {
    public String solution(String letter) {
        String answer = "";

        // 모스 부호 사전 만들기
        Map<String, String> morseDictionary = new HashMap<>();
        String[] morses = {
            ".-", "-...", "-.-.", "-..", ".", "..-.",
            "--.", "....", "..", ".---", "-.-", ".-..",
            "--", "-.", "---", ".--.", "--.-", ".-.",
            "...", "-", "..-", "...-", ".--", "-..-",
            "-.--", "--.."};
        String lowercase = "abcdefghijklmnopqrstuvwxyz";
        char[] lowercases = lowercase.toCharArray();

        for (int i = 0; i < 26; i++) {
            morseDictionary.put(morses[i], String.valueOf(lowercases[i]));
        }

        String[] encodedLetters = letter.split(" ");

        for (String encodedLetter: encodedLetters) {
            answer = answer.concat(morseDictionary.get(encodedLetter));
        }

        return answer;
    }
}
```

- 알게된 점
1. 첫 풀이 때는 add(Key, Value) 메서드로 26번 다 하드코딩했는데, 이번에는 반복문으로 모스부호 사전을 만들어보았다.
2. toCharArray() 메서드의 쓰임새 익혀둬야겠다.