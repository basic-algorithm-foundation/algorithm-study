# [수열과 구간 쿼리 4](https://school.programmers.co.kr/learn/courses/30/lessons/181922)
```java
class Solution {
    public int[] solution(int[] arr, int[][] queries) {
        // s보다 크고 e보다 작은 i를 구한다.
        for(int[] query: queries) {
            int s = query[0];
            int e = query[1];
            int k = query[2];
            for (int i = s; s < e+1; s++) {
                if (s % k == 0) {
                    // i % k == 0 이라면 arr[i]를 1 올려준다.
                    arr[s] ++;
                }
            }
        }
        return arr;
    }
}
```