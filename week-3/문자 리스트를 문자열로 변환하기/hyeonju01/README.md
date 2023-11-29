# [문자 리스트를 문자열로 변환하기](https://school.programmers.co.kr/learn/courses/30/lessons/181941)
```java
class Solution {
    public String solution(String[] arr) {
        String answer = "";
        for(int i = 0; i < arr.length; i++) {
            answer += arr[i];
        }
        return answer;
    }
}
```

- for문 대신 stream에 익숙해지면 코딩 테스트에 응시할 때 편할 것 같다. 