# [등차수열의 특정한 항만 더하기](https://school.programmers.co.kr/learn/courses/30/lessons/181931)
```java
class Solution {
    public int solution(int a, int d, boolean[] included) {
        int answer = 0;

        for (int i = 0; i < included.length; i++) {
            if (included[i] == true) {
                answer = answer + (a + d * i);
            }
        }

        return answer;
    }
}
```