# [숨어있는 숫자의 덧셈 (1)](https://school.programmers.co.kr/learn/courses/30/lessons/120851)
```java
class Solution {
    public int solution(String my_string) {
        int answer = 0;
        char[] charArr = my_string.toCharArray();
        
        for(char c: charArr) {
            if (Character.isDigit(c)) {
                answer += Integer.parseInt(Character.toString(c));
            }
        }
        
        return answer;
    }
}
```