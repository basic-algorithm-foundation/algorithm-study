# [코드 처리하기](https://school.programmers.co.kr/learn/courses/30/lessons/181932)
```java
class Solution {
    public String solution(String code) {
        String answer = "";
        int mode = 0;
        String ret = "";

        for(int i = 0; i < code.length(); i++) {
            if (mode == 0) {
                if (code.charAt(i) != '1') {
                    if (i % 2 == 0 || i % 2 == 2) {
                        ret = ret + code.charAt(i);
                    }
                } else {
                    mode = 1;
                }
            } else {
                if (code.charAt(i) != '1') {
                    if (i % 2 == 1) {
                        ret = ret + code.charAt(i);
                    }
                } else {
                    mode = 0;
                }
            }
        }
        if (ret == "") {
            answer = "EMPTY";
        } else {
            answer = ret;
        }


        return answer;
    }
}
```