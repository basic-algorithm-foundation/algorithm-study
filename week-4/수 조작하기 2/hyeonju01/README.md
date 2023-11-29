# [수 조작하기 2](https://school.programmers.co.kr/learn/courses/30/lessons/181925)
```java
class Solution {
    public String solution(int[] numLog) {
        String answer = "";
        for (int i = numLog.length-1; i > 0; i--) {
            int num = numLog[i] - numLog[i-1];
            // 1 -> "w"
            // -1 -> "s"
            // 10 -> "d"
            // -10 -> "a"
            switch (num) {
                case 1:
                    answer = "w" + answer;
                    break;
                case -1:
                    answer =  "s" + answer;
                    break;
                case 10:
                    answer = "d" + answer;
                    break;
                case -10:
                    answer = "a" + answer;
                    break;
            }
        }
        return answer;
    }
}
```