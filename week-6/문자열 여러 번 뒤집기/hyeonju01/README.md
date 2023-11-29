# [문자열 여러 번 뒤집기](https://school.programmers.co.kr/learn/courses/30/lessons/181913)
```java
class Solution {
    public String solution(String my_string, int[][] queries) {
        StringBuilder sb = new StringBuilder(my_string);

        for(int[] query: queries) {
            int s = query[0];
            int e = query[1];
            StringBuilder subStr = new StringBuilder(sb.substring(s, e+1));
            subStr = subStr.reverse();
            sb = sb.replace(s, e+1, String.valueOf(subStr));
        }
        return String.valueOf(sb);
    }
}
```

- 알게된 점
1. StringBuilder와 String은 동명 메소드가 있는데, type이 다르므로 사용 시 주의하자..
   - e.g. substring(), replace() ..