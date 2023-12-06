# [2차원으로 만들기](https://school.programmers.co.kr/learn/courses/30/lessons/120842)
```java
class Solution {
    public int[][] solution(int[] num_list, int n) {
        int[][] answer = new int[num_list.length/n][n];
        int idx = 0;

        while(idx < num_list.length){
            for(int j = 0; j < answer.length; j++) {
                for(int k = 0; k < n; k++) {
                    answer[j][k] = num_list[idx];
                    idx ++;
                }
            }
        }

        return answer;
    }
}
```

- 알게된 점
2차원 배열의 row와 column이 헷깔리지 않도록 공부하자.