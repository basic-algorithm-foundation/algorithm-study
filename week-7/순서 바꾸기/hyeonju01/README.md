[순서 바꾸기](https://school.programmers.co.kr/learn/courses/30/lessons/181891)
```java
class Solution {
    public int[] solution(int[] num_list, int n) {
        int listLen = num_list.length;
        
        int[] answer = new int[listLen];
        int idx = n;
        // {2, 1, 6} 0, 1, 2
        for(int i = 0; i < listLen; i++) {
            if (idx < listLen) {
            answer[i] = num_list[idx];
            idx ++;
            } else {
                idx = idx - listLen;
                answer[i] = num_list[idx];
                idx ++;
            }
        }
        
        return answer;
    }
}
```