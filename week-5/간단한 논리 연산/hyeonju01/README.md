# [간단한 논리 연산](https://school.programmers.co.kr/learn/courses/30/lessons/181917)
```java
class Solution {
    public boolean solution(boolean x1, boolean x2, boolean x3, boolean x4) {
        boolean answer = true;

        if ((x1 || x2 ? true: false) && (x3 || x4? true: false)) {
            return true;
        } else {
            return false;
        }
    }
}
```