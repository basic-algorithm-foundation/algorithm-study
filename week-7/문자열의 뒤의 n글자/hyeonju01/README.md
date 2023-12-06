# [문자열의 뒤의 n글자](https://school.programmers.co.kr/learn/courses/30/lessons/181910)
```java
class Solution {
    public String solution(String my_string, int n) {

        int s = my_string.length() - n; // 14 - 11 = 3
        int e = my_string.length();
        
        return my_string.substring(s, e);
    }
}
```

- 메서드가 있는지 찾아봐야겠다.