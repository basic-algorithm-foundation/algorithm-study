[배열의 길이에 따라 다른 연산하기](https://school.programmers.co.kr/learn/courses/30/lessons/181854)
```java
class Solution {
    public int[] solution(int[] arr, int n) {
        int arrLen = arr.length;
        int num = 0;
        
        if (arrLen % 2 == 0) {
            num = 1;
        }
        
        for (int i = num; i < arrLen; i += 2) {
            arr[i] += n;
        }
        
        return arr;
    }
}
```