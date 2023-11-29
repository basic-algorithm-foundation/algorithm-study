# [flag에 따라 다른 값 반환하기](https://school.programmers.co.kr/learn/courses/30/lessons/181933)
```java
class Solution {
    public int solution(int a, int b, boolean flag) {
        int answer = 0;
        
        if(!flag) {answer = a - b;} 
        else {answer = a+b;}
        
        return answer;
    }
}
```