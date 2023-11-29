# [홀짝 구분하기](https://school.programmers.co.kr/learn/courses/30/lessons/181944)
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String even = " is even";
        String odd = " is odd";
        
        int n = sc.nextInt();
        if (n % 2 == 0) {
            System.out.println(n+even);
        } else {
            System.out.println(n+odd);
        }
        
    }
}
```

- 궁금한 점
가독성을 어떻게 높여야 할지 궁금함