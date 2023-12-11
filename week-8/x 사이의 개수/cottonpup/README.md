```js
function solution(myString) {
    const convertedArr = myString.split('x');
    for(let i = 0; i < convertedArr.length; i++){
        convertedArr[i] = convertedArr[i].length
    }
    return convertedArr;
}
```
