[할 일 목록](https://school.programmers.co.kr/learn/courses/30/lessons/181885)
```java
import java.util.ArrayList;
class Solution {
    public String[] solution(String[] todo_list, boolean[] finished) {
        String[] answer = {};
        int todoLen = todo_list.length;
        int finishedLen = finished.length;
        
        ArrayList<String> notFinished_list = new ArrayList<>();
        
        for(int i = 0; i < finishedLen; i++) {
            if (!finished[i]) {
                notFinished_list.add(todo_list[i]);
            }
        }
        
        return notFinished_list.stream().toArray(String[]::new);
    }
}
```