# [직각삼각형 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/120823)
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i = 0; i < n; i++) {
            for(int j = 0; j < i+1 ;j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

- 알게된 점
1. 별 찍기는 언제 풀어도 헷깔리는데, 노트에 쓰면서 규칙을 찾으면 풀 수 있다.