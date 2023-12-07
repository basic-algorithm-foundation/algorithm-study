# [첫 번째로 나오는 음수](https://school.programmers.co.kr/learn/courses/30/lessons/181896)
```java
class Solution {
    public int solution(int[] num_list) {
        int answer = 0;
        int minusNum = 0;
        for(int i = 0; i < num_list.length; i++) {
            if (num_list[i] < 0) {
                answer = i;
                minusNum = num_list[i];
                break;
            } else {
                continue;
            }
        }

        if (minusNum < 0) {
            return answer;
        } else {
            return -1;
        }

    }
}
```