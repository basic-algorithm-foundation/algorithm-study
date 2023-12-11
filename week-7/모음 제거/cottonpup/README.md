```js
function solution(my_string) {
    let result = ''
    const vowels = ['a', 'e', 'i', 'o', 'u']
    
    for(str of my_string){
        result += vowels.includes(str) ? '' : str;
    }

    
    return result;
}
```
- `includes`메서드 순서를 틀려서 애먹었다..
