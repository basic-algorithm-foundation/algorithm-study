```js
function solution(my_string, index_list) {
    let result = '';
    index_list.forEach(i => {
        result += my_string[i]
    })
    return result
}
```