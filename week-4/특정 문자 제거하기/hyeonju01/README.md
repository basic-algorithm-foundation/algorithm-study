# [특정 문자 제거하기](https://school.programmers.co.kr/learn/courses/30/lessons/120826)
```java
class Solution {
    public String solution(String my_string, String letter) {
        String answer = "";
        for(int i = 0; i < my_string.length(); i++) {
            String word = Character.toString(my_string.charAt(i));
            if (!word.equals(letter)) {
                answer = answer + my_string.charAt(i);
            }
        }
        return answer;
    }
}
```

- 알게된 점
1. 무작정 반복문으로 풀기보다는 메서드를 익혀 사용하는 버릇을 들여야겠다.