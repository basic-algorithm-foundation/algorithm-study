# [길이에 따른 연산](https://school.programmers.co.kr/learn/courses/30/lessons/181879)
```java
class Solution {
    public int solution(int[] num_list) {
        int answer;

        if (num_list.length >= 11) {
            answer = 0;
            for(int i = 0; i < num_list.length; i++) {
                answer = answer + num_list[i];
            }
        } else {
            answer = 1;
            for(int i = 0; i < num_list.length; i++) {
                answer = answer * num_list[i];
            }
        }
        return answer;
    }
}
```
- 곱셈할 때 answer 값을 1로 초기화 해야했다.