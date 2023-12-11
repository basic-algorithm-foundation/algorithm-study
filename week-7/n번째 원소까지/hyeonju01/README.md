[n 번째 원소까지](https://school.programmers.co.kr/learn/courses/30/lessons/181889)
```java
class Solution {
    public int[] solution(int[] num_list, int n) {
        int[] answer = new int[n];
        for(int i = 0; i < n; i++) {
            answer[i] = num_list[i];
        }
        return answer;
    }
}
```