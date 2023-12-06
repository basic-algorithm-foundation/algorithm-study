# [배열 만들기 5](https://school.programmers.co.kr/learn/courses/30/lessons/181912)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(String[] intStrs, int k, int s, int l) {
        // int[] answer = {};
        ArrayList<Integer> list = new ArrayList<>();
        // s = 인덱스 , l = 문자열 길이, k = 비교대상
        for(String str: intStrs) {
            String sliced = str.substring(s, s+l);
            int slicedNum = Integer.valueOf(sliced);
            if (slicedNum > k) {
                list.add(slicedNum);
            }
        }
        
        return list.stream().mapToInt(Integer::intValue).toArray();
    }
}
```