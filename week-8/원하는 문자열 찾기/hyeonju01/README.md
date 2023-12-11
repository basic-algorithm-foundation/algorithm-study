[원하는 문자열 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/181878)
```java
class Solution {
    public int solution(String myString, String pat) {
        int answer = 0;

        myString = myString.toLowerCase();
        int myStrLen = myString.length();

        pat = pat.toLowerCase();
        int patLen = pat.length();

        if (myStrLen < patLen)  {
            answer = 0;
        } else if (myStrLen == patLen) {
            if (!myString.equals(pat)) {
                answer = 0;
            } else {
                answer = 1;
            }
        } else {
            for (int i = 0; i <= myStrLen - patLen; i++) {
                String sub = myString.substring(i, i + patLen);
                if (pat.equals(sub)) {
                    answer = 1;
                }
            }
        }
        return answer;
    }
}
```

- 조건문 속 비교 대상을 잘못 적어 실수했다.