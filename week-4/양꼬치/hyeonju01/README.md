# [양꼬치](https://school.programmers.co.kr/learn/courses/30/lessons/120830)
```java
class Solution {
    public int solution(int n, int k) {
        int LambTotal = 0;
        int sodaTotal = 0;

        LambTotal = n * 12000;

        if (n < 10) {
            sodaTotal = k * 2000;
        } else {
            sodaTotal = (k - (n / 10)) * 2000;
        }

        return LambTotal + sodaTotal;
    }
}
```