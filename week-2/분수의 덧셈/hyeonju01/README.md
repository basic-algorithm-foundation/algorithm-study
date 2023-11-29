# [분수의 덧셈](https://school.programmers.co.kr/learn/courses/30/lessons/120808)
```java
class Solution {
    public int[] solution(int numer1, int denom1, int numer2, int denom2) {
        int[] answer = {};


        // 공통분모
        int commonDenom = 0;

        // 최소공배수
        if (denom1 % demon2 == 0) {
            commonDenom = denom1;
            numer2 = numer2 * (denom1 / denom2);
        } else if(denom2 % denom1 == 0) {
            commonDenom = denom2;
            numer1 = numer1 * (denom2 / denom1);
        } else { // 서로소 
            commonDenom = denom1 * denom2;
            numer1 = numer1 * denom2;
            numer2 = numer2 * denom1;
        }

        // 분자 덧셈
        outputNumer = numer1 + numer2;

        int idx = 1;

        // 분모를 분자로 나누었을 때 나머지가 없을 동안 실행
        while(true) {
            if (commonDenom % idx == 0 & outputNumer % idx == 0) {
                commonDenom = commonDenom / idx;
                outputNumer = outputNumer / idx;
            }
        }


        return answer;
    }
}
```

- 알게된 점
1. 마지막에 두 분수의 합을 기약 분수로 나타내는 과정에서 로직이 떠오르지 않았다.. 