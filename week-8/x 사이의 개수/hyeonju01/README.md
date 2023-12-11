[x 사이의 개수](https://school.programmers.co.kr/learn/courses/30/lessons/181867)
```java
class Solution {
    public int[] solution(String myString) {
        
        String[] splitted = myString.split("x", -1);
        int arrNum = splitted.length;
        
        int[] answer = new int[arrNum];
        
        for(int i = 0; i < arrNum; i++) {
            int strLen = splitted[i].length();
            answer[i] = strLen;
        }
            
        return answer;
    }
}
```

- split(regex, limit)
  limit을 -1로 두면 맨 뒤의 빈 값도 포함하여 split 결과 배열에 넣어줌