# [주사위 게임 2](https://school.programmers.co.kr/learn/courses/30/lessons/181930)
```java
class Solution {
    public int solution(int a, int b, int c) {
        int answer = 0;

        if (a != b & b != a & a != c) {
            answer = a + b + c;
        }

        if ((a == b & b != c) || (a == c & b != c) || (b == c & a != c)) {
            answer = (a + b + c) * (a*a + b*b + c*c);
        }

        if (a == b & b == c) {
            answer = (a + b + c) * (a*a + b*b + c*c) * (a*a*a + b*b*b + c*c*c);
        }

        return answer;
    }
}
```

- 알게된 점
1. abc
2. def
3. ghi