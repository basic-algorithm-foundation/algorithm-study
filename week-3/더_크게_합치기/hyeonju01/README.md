# [더 크게 합치기](https://school.programmers.co.kr/learn/courses/30/lessons/181939)
```java
class Solution {
    public int solution(int a, int b) {
        int answer = 0;
        String ab = String.valueOf(a) + String.valueOf(b);
        String ba = String.valueOf(b) + String.valueOf(a);

        int intAB = Integer.valueOf(ab);
        int intBA = Integer.valueOf(ba);

        return (intAB > intBA) ? intAB : intBA ;
    }
}
```

- 알게된 점
1. String과 int 타입 모두 valueOf()라는 메소드를 가진다. 사용에 주의한다..