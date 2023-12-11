[문자열 정수의 합](https://school.programmers.co.kr/learn/courses/30/lessons/181849)

```java
class Solution {
    public int solution(String num_str) {
        int answer = 0;
        String[] numArr = num_str.split("");
        for(String num: numArr) {
            int intNum = Integer.parseInt(num);
            answer += intNum;
        }
        return answer;
    }
}
```