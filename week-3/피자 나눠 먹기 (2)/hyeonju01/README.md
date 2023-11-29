# [피자 나눠 먹기 (2)](https://school.programmers.co.kr/learn/courses/30/lessons/120815)
```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        int idx = 1;

        while(true) {

            if ((n * idx) % 6 != 0) {
                idx ++;

            } else {
                answer = (n * idx) / 6;
                break;
            }

        }

        return answer;

    }
}
```

- 알게된 점
1. while문의 스코프를 잘 몰라서 헤맸다. continue, break의 스코프를 잘 알아둬야겠다. 기본기에 충실하자.