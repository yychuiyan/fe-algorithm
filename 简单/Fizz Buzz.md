## 题目 [Fizz Buzz](https://leetcode.cn/problems/fizz-buzz/)

> 给你一个整数 n ，找出从 1 到 n 各个整数的 Fizz Buzz 表示，并用字符串数组 answer（下标从 1 开始）返回结果，其中：
>
> - answer[i] == "FizzBuzz" 如果 i 同时是 3 和 5 的倍数。
> - answer[i] == "Fizz" 如果 i 是 3 的倍数。
> - answer[i] == "Buzz" 如果 i 是 5 的倍数。
> - answer[i] == i （以字符串形式）如果上述条件全不满足。

### 解题思路

声明一个字符串数组`answer`，给定一个值进行遍历，遍历的过程中使用If进行判断，如果是`i`同时是 `3` 和 `5` 的倍数，则`push` "FizzBuzz"，如果 `i` 是 `3` 的倍数则`push` "Fizz"，如果 `i` 是 `5` 的倍数，则`push` "Buzz"，否则返回将该数值转换为字符串传入到`answer`数组中

### 解题方法

- 声明一个字符串数组
- 使用for循环进行遍历，在for循环内部使用if进行判断
- 如果是`i`同时是 `3` 和 `5` 的倍数，则`push` "FizzBuzz"，如果 `i` 是 `3` 的倍数则`push` "Fizz"，如果 `i` 是 `5` 的倍数，则`push` "Buzz"，否则返回将该数值转换为字符串传入到`answer`数组中。

### 代码输出

```javascript
/**
 * @param {number} n
 * @return {string[]}
 */
var fizzBuzz = function(n) {
    let answer=[];
    for(let i=1; i<=n;i++){
        if(i % 3===0 && i % 5 ===0){
            answer.push("FizzBuzz")
        }else if(i % 3===0){
            answer.push("Fizz")
        }else if(i % 5===0){
            answer.push("Buzz")
        }else{
            answer.push(i+"")
        }
    }
    return answer;
};
```
