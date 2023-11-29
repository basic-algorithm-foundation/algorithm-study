# [문자 반복 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/120825)
```java
class Solution {
    public String solution(String my_string, int n) {
        String answer = "";
        for(int i = 0; i < my_string.length(); i++) {
            for(int j = 0; j < n; j++) {
                answer = answer + my_string.charAt(i);
            }
        }
        return answer;
    }
}
```