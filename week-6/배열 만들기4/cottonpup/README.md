# 틀린 답안
```js
function solution(arr) {

    const stk = [];
    for(let i = 0; i < arr.length; i++){
        if(stk.length === 0){
            stk.push(arr[i]);
            i++; // Incremented here
        } else {
            if (stk[stk.length - 1] < arr[i]) {
                stk.push(arr[i]);
                i++; // Incremented here
            } else if(stk[stk.length - 1] >= arr[i]){
                stk.pop();
            }
        } 
       
    }
    return stk;
}

```
- for loop 을 사용해서 `i`를 두번 증가시키는 것이 문제였다 ㅠㅠㅠ 
# 고쳐진 버전
```js
function solution(arr) {

    const stk = [];
    let i = 0; // Initialize i outside of the loop

    while (i < arr.length) {
        if (stk.length === 0) {
            stk.push(arr[i]);
            i++; // Increment i only once when stk is empty
        } else {
            if (stk[stk.length - 1] < arr[i]) {
                stk.push(arr[i]);
                i++; // Increment i only once when stk's last element is smaller
            } else if (stk[stk.length - 1] >= arr[i]) {
                stk.pop();
            }
        } 
    }
    return stk;
}
```