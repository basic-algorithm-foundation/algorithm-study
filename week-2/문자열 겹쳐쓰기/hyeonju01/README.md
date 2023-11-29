# [문자열 겹쳐쓰기](https://school.programmers.co.kr/learn/courses/30/lessons/181943)
```java
class Solution {
    public String solution(String my_string, String overwrite_string, int s) {
        String answer = "";
        int e = s + overwrite_string.length();
        StringBuffer sb = new StringBuffer(my_string);
        sb.replace(s, e, overwrite_string);
        answer = sb.toString();
        return answer;
    }
}
```

- 알게된 점
인덱스 처리를 잘 해야겠다.