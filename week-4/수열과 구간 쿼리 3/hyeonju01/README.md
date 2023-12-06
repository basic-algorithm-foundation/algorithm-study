# [수열과 구간 쿼리 3](https://school.programmers.co.kr/learn/courses/30/lessons/181924)
```java
class Solution {
    public int[] solution(int[] arr, int[][] queries) {
        for (int i = 0; i < queries.length; i++) {

            int firstIdx = queries[i][0];
            int lastIdx = queries[i][1];

            int temp = arr[firstIdx];
            arr[firstIdx] = arr[lastIdx];
            arr[lastIdx] = temp;

        }

        return arr;

    }
}
```