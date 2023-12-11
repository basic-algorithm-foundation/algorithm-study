[소인수분해](https://school.programmers.co.kr/learn/courses/30/lessons/120852)
# ❌️ 실패
```java
static class Solution {
    public int[] solution(int n) {
        int[] answer = {};

        // int[] primeNum = {2, 3, 5, 7, 11};

        int idx = 2;
        ArrayList<Integer> arr = new ArrayList<>();
        while(n != 1) {

            // idx가 소수인지 검증
            if (isPrime(idx)) {
                System.out.println(idx);
                if (n % idx == 0) {
                    System.out.println("n: " + n);
                    System.out.println("idx: " + idx);
                    n = n / idx;
                    if (!arr.contains(idx)) {
                        arr.add(idx);
                    }
                } else {
                    idx ++;
                }
            }
        }

        return arr.stream().mapToInt(Integer::intValue).toArray();
    }

    // num >= 2
    boolean isPrime(int num) {
        int  temp = 0;
        for(int i = 1; i < num + 1; i++) {
            if (num % i == 0) {
                temp++;
            }
        }
        if (temp == 2) {
            return true;
        }

        return false;
    }
}
```

# ⭐️ 성공
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