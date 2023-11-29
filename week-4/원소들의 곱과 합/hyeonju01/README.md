# [원소들의 곱과 합](https://school.programmers.co.kr/learn/courses/30/lessons/181929)
```java
class Solution {
    public int solution(int[] num_list) {
        int answer = 0;
        int sum = 0;
        int multiple = 1;

        for (int i = 0; i < num_list.length; i++) {
            sum = sum + num_list[i];
            multiple = multiple * num_list[i];
        }

        if (multiple < sum*sum) {
            answer = 1;
        } else if (multiple > sum*sum){
            answer = 0;
        }

        return answer;
    }
}
```