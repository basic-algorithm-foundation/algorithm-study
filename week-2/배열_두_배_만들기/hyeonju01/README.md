# [배열 두배 만들기](https://school.programmers.co.kr/learn/courses/30/lessons/120809)
```java
class Solution {
    public int[] solution(int[] numbers) {
        int inputLen = numbers.length;
        int[] answer = new int[inputLen];

        for(int i = 0; i < inputLen; i++) {
            answer[i] = numbers[i] * 2;
        }

        return answer;
    }
}
```

- 알게된 점
1. 정수 배열 원소에 연산을 할 때 stream을 활용하여 연산하는 문법을 익혀야겠다.
2. 변수명 잘 확인하자.