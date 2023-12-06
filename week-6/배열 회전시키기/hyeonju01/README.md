# [배열 회전시키](https://school.programmers.co.kr/learn/courses/30/lessons/120844)
```java
class Solution {
    public int[] solution(int[] numbers, String direction) {
        int[] answer = new int[numbers.length];
        if (direction.equals("right")) {
            for(int i = 0; i < numbers.length; i++) {
                if (i == 0) {
                    answer[i] = numbers[numbers.length - 1];
                } else if (i > 0) {
                    answer[i] = numbers[i - 1];
                }
            }
        } else {
            for (int i = 0; i < numbers.length; i++) {
                if (i == numbers.length - 1) {
                    answer[numbers.length - 1] = numbers[0];
                } else {
                    answer[i] = numbers[i + 1];    
                }
            }
        }
        return answer;
    }
}
```