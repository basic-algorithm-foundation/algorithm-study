[숨어있는 숫자의 덧셈 (1)](https://school.programmers.co.kr/learn/courses/30/lessons/120851)
```javascript
function solution(my_string) {
   let result = 0;
    for(const str of my_string){
        if(Number(str)){
           result += Number(str)
        }
    }
    return result
}
```