# es6语法
 ## 数组
+ foreach

```js
let arr = [1,2,3,,,]
arr.foreach(item => {
    console.log(item)
})
// 输出结果：1 2 3 （空占位不输出）
```
+ find
```js
let arr1 = [1,2,3,,,]
arr1.find(item => {
    console.log(item)
})
// 输出结果: 1 2 3 undefind undefind (输出空占位为undefind)
```
+ filter
```js
let arr2 = [1,2,3,4,1,'a']
let aa = arr2.filter(item => {
    return typeof item == 'string'
})
console.log(aa)
// 输出结果 ['a']
// 过滤符合条件内容
// *特别注意*
 // let arr2 = [1, 2, 3, 4, 1, 'a',{name:'88'}]
    let arr2 = [
        {name:'pan1',age:18},
        { name: 'pan', age: 18 },
        { name: 'pan1', age: 18 },
        { name: 'pan', age: 18 },
    ]
      let aa =  arr2.filter(item => {
            return item.name == 'pan1'
        })
        aa[0].name = 'ddd'
        console.log(aa)
        console.log(arr2)

 // ddd会被追加到arr2中，因为数组对象的地址没有变还是原来的arr2

```
+ some 
``` js
let arr3 = [1,2,3,5,'a']
arr3.some(item => {
    return typeof item == 'string'
})
// some函数为当数组中有一项符合规则时即返回true
```
+ every
``` js
let arr4 = [1,2,3,4,'p']
arr4.every(item => {
    return typeof item == 'string'
})
// every函数为当数组中每一项都符合规则时才返回true，否则返回false
```
+ set
``` js
let arr5 = [1,2,3,1,1]
let arrSet = new Set(arr5)
console.log(arrSet)
// 输出 类数组对象
// set去重功能 在利用...扩展运算符
let ar = [...new Set(arr5)]
// 
arrSet.foreach((value,value2,set) => {
    console.log(value,value2,set)
})
// set 函数只有value值没有下标值
```

