# [특정한 문자를 대문자로 바꾸기](https://school.programmers.co.kr/learn/courses/30/lessons/181873)
```java
class Solution {
    public String solution(String my_string, String alp) {
        String upperAlp = alp.toUpperCase();
        return my_string.replaceAll(alp, upperAlp);
    }
}
```