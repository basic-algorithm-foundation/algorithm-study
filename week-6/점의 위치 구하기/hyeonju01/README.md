# [점의 위치 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/120841)
```java
class Solution {
    public int solution(int[] dot) {
        int x = dot[0]; // x
        int y = dot[1]; // y
        
        if ((x * y) > 0) {
            if (x > 0) {
                return 1;
            } else {
                return 3;
            }
        } else {
            if (x > 0) {
                return 4;
            } else {
                return 2;
            }
        }
    }
}
```