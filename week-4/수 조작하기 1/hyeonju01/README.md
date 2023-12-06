# [수 조작하기 1](https://school.programmers.co.kr/learn/courses/30/lessons/181926)
```java
class Solution {
    public int solution(int n, String control) {
        for (int i = 0; i < control.length(); i++) {
            String c = String.valueOf(control.charAt(i));
            switch (c) {
                case "w":
                    n ++;
                    break;
                case "s":
                    n --;
                    break;
                case "d":
                    n = n + 10;
                    break;
                case "a":
                    n = n - 10;
                    break;
            }
        }
        return n;
    }
}
```