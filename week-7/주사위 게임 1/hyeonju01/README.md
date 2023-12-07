# [주사위 게임 1](https://school.programmers.co.kr/learn/courses/30/lessons/181839)
```java
import java.lang.Math;

class Solution {
    public int solution(int a, int b) {
        int answer = 0;

        // a, b 모두 홀수 -> a*a + b*b
        // a, b 중 하나가 홀수 -> 2 * (a + b)
        // a, b 모두 짝수 -> | a - b |
        if ((a % 2 != 0) && (b % 2 != 0)) {
            return a * a + b * b;
        } else if (((a % 2 != 0) && (b % 2 == 0)) || ((a % 2 == 0) && (b % 2 != 0))) {
            return 2 * (a + b);
        } else {
            return Math.abs(a-b);
        }
    }
}
```