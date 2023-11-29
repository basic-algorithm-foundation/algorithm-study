# [두 수의 나눗셈](https://school.programmers.co.kr/learn/courses/30/lessons/120806)
```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;
        double output = (double)num1 / (double)num2;
        answer = (int)(1000 * output);
        return answer;
    }
}
```

- 알게된 점
1. long, double 등 실수 자료형에 대한 개념이 아직은 불분명하다. 제대로 숙지하자.