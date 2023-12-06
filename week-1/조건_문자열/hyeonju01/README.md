# [조건 문자열](https://school.programmers.co.kr/learn/courses/30/lessons/181934)
```java
class Solution {
    public int solution(String ineq, String eq, int n, int m) {
        int answer = 0;

        // ineq, eq를 붙여서 하나의 string으로 만든다.
        String operator = ineq.concat(eq);

        // 만들어진 연산 기호에 따라 연산을 진행한다. 
        switch(operator) {
            case(">="):
                // 조건
                if (n >= m) {answer = 1;}
                else {answer = 0;}
                break;
            case("<="):
                // 조건
                if (n <= m) {answer = 1;}
                else {answer = 0;}
                break;
            case(">!"):
                // 조건
                if (n > m) {answer =  1;}
                else {answer = 0;}
                break;
            case("<!"):
                // 조건
                if (n < m) {answer =  1;}
                else {answer = 0;}
                break;
        }

        return answer;
    }
}
```

- 연산자 종류별 연산 순서를 기억해둬야겠다. 이항, 삼항 연산자도 익숙해져야겠다.