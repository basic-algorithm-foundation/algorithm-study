# [옷가게 할인 받기](https://school.programmers.co.kr/learn/courses/30/lessons/120818)
```java
class Solution {
    public int solution(int price) {
        double answer = 0;
        if (price >= 10_0000 && price < 30_0000) {
            answer = (double) price * 0.95;
        } else if (price >= 30_0000 && price < 50_0000) {
            answer = (double) price * 0.9;
        } else if (price >= 50_0000) {
            answer = (double) price * 0.8;
        } else {
            answer = (double) price;
        }
        return (int) answer;
    }
}
```