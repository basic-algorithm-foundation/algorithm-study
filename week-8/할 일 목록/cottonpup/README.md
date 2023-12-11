```js
function solution(todo_list, finished) {
    const result = []
    todo_list.forEach((todo, i) => {
        if(!finished[i]){
            result.push(todo)
        }
    })
    return result;
}
```
