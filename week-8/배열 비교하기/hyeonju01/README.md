[배열 비교하기](https://school.programmers.co.kr/learn/courses/30/lessons/181856)
```java
import java.util.*;

class Solution {
    public int solution(int[] arr1, int[] arr2) {
        int answer = 0;
        int arr1Len = arr1.length;
        int arr2Len = arr2.length;
                
        if (arr1Len != arr2Len) {
            if (arr1Len > arr2Len) {
                answer = 1;
            } else {
                answer = -1;
            }
        } else if (arr1Len == arr2Len){
            int arr1Sum = Arrays.stream(arr1).sum();
            int arr2Sum = Arrays.stream(arr2).sum();
            
            if (arr1Sum > arr2Sum) {
                answer = 1;
            } else if (arr1Sum < arr2Sum) {
                answer = -1;
            } else {
                answer = 0;
            }
        }
        
        return answer;
        
    }
}
```

- 정수 배열의 합 구하기
  - stream(arrayName).sum()
- 변수명 잘 적기.. 이런 것에서 실수하지 말자