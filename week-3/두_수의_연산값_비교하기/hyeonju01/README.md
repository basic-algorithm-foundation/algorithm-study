# [두 수의 연산값 비교하기](https://school.programmers.co.kr/learn/courses/30/lessons/181938)
```java
class Solution {
    public int solution(int a, int b) {

        String ab = String.valueOf(a) + String.valueOf(b);
        int doubleAB = 2 * a * b;
        int plusAB = Integer.valueOf(ab);

        if (plusAB >= doubleAB) {
            return plusAB;
        } else {
            return doubleAB;
        }
    }
}
```

- 알게된 점
1. abc
2. def
3. ghi