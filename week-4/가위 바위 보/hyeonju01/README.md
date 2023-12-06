# [가위 바위 보](https://school.programmers.co.kr/learn/courses/30/lessons/120839)
```java
class Solution {
    public String solution(String rsp) {
        String answer = "";
        // 가위(2) lose 바위(0)
        // 바위(0) lose 보(5)
        // 보(5) lose 가위(2)

        for(int i = 0; i < rsp.length(); i++) {
            char input = rsp.charAt(i);
            switch(input) {
                case '2':
                    answer = answer.concat("0");
                    break;
                case '0':
                    answer = answer.concat("5");
                    break;
                case '5':
                    answer = answer.concat("2");
                    break;
            }
        }

        return answer;
    }
}
```