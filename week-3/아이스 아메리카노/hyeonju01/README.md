# [아이스 아메리카노](uhttps://school.programmers.co.kr/learn/courses/30/lessons/120819)
```java
class Solution {
    public int[] solution(int money) {
        int[] answer = {0, 0};
        answer[0] = money/5500;
        answer[1] = money%5500;
        return answer;
    }
}
```