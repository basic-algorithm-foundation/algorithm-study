[배열에서 문자열 대소문자 변환하기](https://school.programmers.co.kr/learn/courses/30/lessons/181875)
```java
class Solution {
    public String[] solution(String[] strArr) {
        int arrLen = strArr.length;
        for (int i = 0; i < arrLen; i++) {
            if (i%2 == 0) {
                strArr[i] = strArr[i].toLowerCase();
            } else {
                strArr[i] = strArr[i].toUpperCase();
            }
        }
        return strArr;
    }
}
```