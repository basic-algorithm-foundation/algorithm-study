# [배열 뒤집기](https://school.programmers.co.kr/learn/courses/30/lessons/120821)
```java
class Solution {
    public int[] solution(int[] num_list) {
        int[] answer = new int[num_list.length];
        int end = num_list.length - 1;
        int start = 0;
        for(int i = start; i < answer.length; i++) {
            answer[i] = num_list[end];
            end--;
        }
        return answer;
    }
}
```