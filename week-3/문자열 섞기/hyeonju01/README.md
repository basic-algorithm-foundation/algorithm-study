# [문자열 섞기](https://school.programmers.co.kr/learn/courses/30/lessons/181942)
```java
class Solution {
    public String solution(String str1, String str2) {
        String answer = "";

        int n = str1.length();

        for(int i = 0; i < n; i++) {
            answer = answer + Character.toString(str1.charAt(i)) + Character.toString(str2.charAt(i));
        }

        return answer;
    }
}
```