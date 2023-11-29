# [배열의 평균값](https://school.programmers.co.kr/learn/courses/30/lessons/120817)
```java
class Solution {
    public double solution(int[] numbers) {
        double answer = 0;
        int sum = 0;
        for (int number: numbers) {
            sum = sum + number;
        }
        answer = (double)sum / numbers.length;
        return answer;
    }
}
```