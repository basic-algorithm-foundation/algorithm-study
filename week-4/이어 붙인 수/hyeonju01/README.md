# [이어 붙인 수](https://school.programmers.co.kr/learn/courses/30/lessons/181928)
```java
class Solution {
    public int solution(int[] num_list) {
        String oddNums = "";
        String evenNums = "";

        for (int num: num_list) {
            if (num % 2 == 0) {
                evenNums = evenNums + Integer.toString(num);
            } else {
                oddNums = oddNums + Integer.toString(num);
            }
        }
        return Integer.parseInt(evenNums) + Integer.parseInt(oddNums);
    }
}
```

- 알게된 점
1. abc
2. def
3. ghi