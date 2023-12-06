# [조건에 맞게 수열 변환하기 3](https://school.programmers.co.kr/learn/courses/30/lessons/181835)
```java
class Solution {
    public int[] solution(int[] arr, int k) {

        for(int i = 0; i < arr.length; i++) {
            if(k % 2 == 0) {
                arr[i] = arr[i] + k;
            } else {
                arr[i] = arr[i] * k;
            }
        }

        return arr;
    }
}
```