# [조건에 맞게 수열 변환하기1](https://school.programmers.co.kr/learn/courses/30/lessons/181882)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(int[] arr) {
        int arrLength = arr.length; // 배열 길이
        ArrayList<Integer> arrList = new ArrayList<>();

        for(int i = 0; i < arrLength; i++) {
            if (arr[i] >= 50 && arr[i] % 2 == 0) { // 50보다 큰 짝수
                arrList.add(arr[i]/2);
            } else if (arr[i] < 50 && arr[i] % 2 == 1) { // 50보다 작은 홀수 
                arrList.add(arr[i]*2);
            } else { // 변경 조건에 해당하지 않는 경우
                arrList.add(arr[i]);
            }
        }

        return arrList.stream().mapToInt(Integer::intValue).toArray();
    }
}
```