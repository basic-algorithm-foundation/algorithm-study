# [a와 b 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/181951)
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

- %s %d 등으로 문자열과 함께 출력하는 방법을 사용하면 더 깔끔할 것 같다. 익숙하지 않아 그냥 두 줄로 출력함.