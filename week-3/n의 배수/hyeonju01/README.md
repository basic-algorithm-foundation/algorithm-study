# [n의 배수](https://school.programmers.co.kr/learn/courses/30/lessons/181937)
```java
class Solution {
    public int solution(int num, int n) {

        return (num % n == 0) ? 1: 0;
    }
}
```

- 알게된 점
삼항 연산자로 처리하니 간단하고 편하고 좋다.. 