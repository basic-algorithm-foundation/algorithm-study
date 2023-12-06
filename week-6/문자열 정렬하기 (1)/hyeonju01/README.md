# [문자열 정렬하기 (1)](https://school.programmers.co.kr/learn/courses/30/lessons/120850)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(String my_string) {
        int[] answer = {};
        ArrayList<Integer> list = new ArrayList<>();
        
        char[] charArr = my_string.toCharArray();
        
        for(int i = 0; i < charArr.length; i++) {
            if (Character.isDigit(charArr[i])) {
                list.add(Integer.parseInt(String.valueOf(charArr[i])));
            }
        }
        
        return list.stream().mapToInt(Integer::intValue).sorted().toArray();
    }
}
```

- 알게된 점
1. 이외에도 숫자의 아스키코드로 숫자를 추출하는 방법, 정규식으로 replaceAll하여 문자열을 삭제하는 방법 등등이 있었다.
2. stream 정렬하는 방법 알아둬야겠다.