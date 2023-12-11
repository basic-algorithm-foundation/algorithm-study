[꼬리 문자열](https://school.programmers.co.kr/learn/courses/30/lessons/181841)
```java
class Solution {
    public String solution(String[] str_list, String ex) {
        String answer = "";
        for(String str: str_list) {
            if (!str.contains(ex)) {
                answer = answer.concat(str);
            }
        }
        return answer;
    }
}
```