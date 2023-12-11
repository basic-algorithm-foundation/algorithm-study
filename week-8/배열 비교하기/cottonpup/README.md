```js
function solution(arr1, arr2) {
    if(arr1.length === arr2.length){
       const sumOfArr1 = arr1.reduce((acc, cur) => acc + cur);
       const sumOfArr2 = arr2.reduce((acc, cur) => acc + cur);
        if(sumOfArr1 > sumOfArr2){
            return 1;
        } else if(sumOfArr1 < sumOfArr2){
            return -1;
        } else {
            return 0;
        }
    } else if(arr1.length < arr2.length){
        return -1;
    } else if(arr1.length > arr2.length){
        return 1;
    }
}
```
