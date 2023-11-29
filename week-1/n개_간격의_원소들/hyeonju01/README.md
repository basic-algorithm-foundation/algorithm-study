# [n개 간격의 원소들](https://school.programmers.co.kr/learn/courses/30/lessons/181888)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(int[] num_list, int n) {
        int[] answer = {};

        ArrayList<Integer> numbers = new ArrayList<>();

        for(int i = 0; i < num_list.length; i=i+n) {
            numbers.add(num_list[i]);
        }

        return answer = numbers.stream().mapToInt(i -> i).toArray();
    }
}
```
- 항상 for 문 조건식 변수 값을 1씩만 올리는 걸 사용했어서 문법이 헷갈려서 오히려 길을 돌아갔다... 기본기의 중요성.