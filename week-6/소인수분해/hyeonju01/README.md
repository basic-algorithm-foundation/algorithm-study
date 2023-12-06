# [소인수분해](https://school.programmers.co.kr/learn/courses/30/lessons/120852)
```java
import java.util.ArrayList;

class Solution {
    public int[] solution(int n) {
        int idx = 2;
        ArrayList<Integer> arr = new ArrayList<>();
        
        while(idx <= n) {
            if (isPrime(idx)) {
                if (n % idx == 0) {
                    n /= idx;
                    if (!arr.contains(idx)) {
                        arr.add(idx);
                    }
                }
            }
            idx ++;
        }
        return arr.stream().mapToInt(Integer::intValue).toArray();
    }
    
    // 소수 판별 메서드
    boolean isPrime(int num) {
        int tmp = 0; // 약수의 갯수
        for(int i = 1; i < num+1; i++) {
            if (num % i == 0) {
                tmp ++;
            }
        }
        
        if (tmp == 2) { // 약수가 하나인 1, 약수가 여러 개인 수는 소수가 아니다. 
            return true;
        } else {
            return false;
        }
    }
}
```

- 반복문 탈출 조건을 꼼꼼히 생각하자