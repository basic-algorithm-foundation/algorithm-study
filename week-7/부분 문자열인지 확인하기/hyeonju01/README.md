[부분 문자열인지 확인하기](https://school.programmers.co.kr/learn/courses/30/lessons/181843)
```java
class Solution {
    public int solution(String my_string, String target) {
        int answer = 0;
        int strLen = my_string.length();
        int targetLen = target.length();
        
        for(int i = 0; i <= strLen - targetLen; i++) {
            String subStr = my_string.substring(i, i+targetLen);
            if (target.equals(subStr)) {
                answer = 1;
                break;
            }
        }
        
        return answer;
    }
}
```