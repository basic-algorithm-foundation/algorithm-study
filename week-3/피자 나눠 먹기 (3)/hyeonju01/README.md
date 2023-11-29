# [피자 나눠 먹기 (3)](https://school.programmers.co.kr/learn/courses/30/lessons/120816)
```java
class Solution {
    public int solution(int slice, int n) {
        int answer = 0;
        while(true) {
            if (n % slice == 0) {
                answer = n / slice;
                break;
            } else {
                n++;
                continue;
            }
        }
        return answer;
    }
}
```