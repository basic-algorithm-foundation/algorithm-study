(소인수분해)(https://school.programmers.co.kr/learn/courses/30/lessons/120852)
# 포기
```javascript
function solution(n) {
    const result = [];
    let smallestNumber = 2;
    for(let i = 0; i < n; i++){
        if(n % smallestNumber === 0) {
            if(!result.includes(smallestNumber)){
                result.push(smallestNumber)                
            }
            n = n / smallestNumber
        } else {
          if(!result.includes(n)){
            result.push(n)
          }
        }
    }
    
    return result;

}
```
- 두 개의 테스트를 통과하였으나, n이 큰 수이고 여러 소인수를 가질 때 가장 작은 소수인 smallestNumber를 어떻게 증가시켜야 할지 고민했다.

# 고친 코드
```javascript
function solution(n) {
    const result = [];
    for (let i = 2; i <= n; i++) {
        while (n % i === 0) {
            if(!result.includes(i)){
                result.push(i);
            }
            n = n / i;
        }
    }
    return result;
}
```
- 두 개의 테스트를 통과하였으나, n이 큰 수이고 여러 소인수를 가질 때 가장 작은 소수인 smallestNumber를 어떻게 증가시켜야 할지 고민했다.