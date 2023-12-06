# [부분 문자열 이어 붙여 문자열 만들기](https://school.programmers.co.kr/learn/courses/30/lessons/181911)
```java
class Solution {
    public String solution(String[] my_strings, int[][] parts) {
        String answer = "";
        
        for(int i = 0; i < my_strings.length; i++) {
            String myStr = my_strings[i];
            int s = parts[i][0];
            int e = parts[i][1];
            answer = answer.concat(myStr.substring(s, e+1));
        }
        
        return answer;
    }
}
```