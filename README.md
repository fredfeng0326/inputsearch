# inputsearch

> input search function

```
querySearch(queryString, cb) {
      var restaurants = this.restaurants;
      var results = queryString ? restaurants.filter(this.createFilter(queryString)) : restaurants;
      // 调用 callback 返回建议列表的数据
      cb(results);
},
createFilter(queryString) {
      return (restaurant) => {
        return (restaurant.value.toLowerCase().indexOf(queryString.toLowerCase()) === 0);
      };
}
```
这是例子的中算法。其实很简单，就是indexOf的简单应用。
但是这个```===0```只能从开头匹配。全字段匹配就要改成```>-1``` 

[演示页面](https://fredfeng0326.github.io/inputsearch/)
![image](https://github.com/fredfeng0326/inputsearch/blob/master/img/after.png)
![image](https://github.com/fredfeng0326/inputsearch/blob/master/img/before.png)
## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

``` 




