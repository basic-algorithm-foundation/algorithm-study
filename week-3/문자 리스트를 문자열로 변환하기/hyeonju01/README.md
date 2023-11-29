# [problem-title](url)
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