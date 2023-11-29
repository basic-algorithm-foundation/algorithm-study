# [개미 군단](https://school.programmers.co.kr/learn/courses/30/lessons/120837)
```java
class Solution {
    public int solution(int hp) {
        int answer = 0;
        final int general = 5;
        final int soldier = 3;
        final int worker = 1;

        // 가장 적은 수의 병력을 데려가도록
        while(hp > 0) {
            if (hp >= 5) { // 장군개미
                answer += hp / general;
            }
            hp = hp % general;

            if (hp >= 3) { // 병정개미
                answer += hp / soldier;
            }
            hp = hp % soldier;

            if (hp < 3){
                answer += hp / worker;
            }
            hp = hp % worker;
        }

        return answer;
    }
}
```

- 알게된 점
1. 조건문 숫자 범위 주의하기. 숫자 포함 여부에 따라 분기점이 달라져서 답이 나오지 않음