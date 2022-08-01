# Array 对象

- #### 检测是否为数组

  ```js
  //1. instanceof 运算符
  var arr = [];
  var obj = {};
  console.log(arr instanceof Array); //true
  console.log(obj instanceof Array); //false
  
  //2. Array.isArray(参数) 方法 H5新增
  console.log(Array.isArray(arr)); //true
  console.log(Array.isArray(obj)); //false
  ```

  ##### 补充：反转数组

  ```js
  //反转数组
  function reverse(arr) {
      if (arr instanceof Array) {
          var newArr = [];
          for (var i = arr.length - 1; i >= 0; i--) {
              newArr[newArr.length] = arr[i];
          }
          return newArr;
      } else {
          return '这个参数必须是数组格式[value,value,...]'
      }
  }
  console.log(reverse([1, 2, 3]));
  console.log(reverse(1, 2, 3));
  ```

  

- #### 添加数组元素

  ```js
  //1. push() 在数组末尾添加一个或多个数组元素
  var arr = [1, 2, 3];
  arr.push(4, 'hi'); //push完毕之后返回值是新数组的长度
  console.log(arr);
  
  //2. unshift() 在数组开头添加一个或多个数组元素
  arr.unshift('red', 8); //unshift完毕之后返回值是新数组的长度
  console.log(arr);
  ```

  

- #### 删除数组元素

  ```js
  //1. pop() 删除数组的最后一个元素
  var arr = ["red", 8, 1, 2, 3, 4, "hi"];
  arr.pop(); //里面不跟参数，返回值是删除的元素值
  console.log(arr);
  
  //2. shift() 删除数组的第一个元素
  arr.shift(); //里面不跟参数，返回值是删除的元素值
  console.log(arr);
  ```

  

- #### 数组排序

  ```js
  //1. reverse() 反转数组
  var arr = [1, 2, 3];
  arr.reverse();
  console.log(arr);
  
  //2. sort() 冒泡排序
  var arr1 = [2, 42, 1, 66, 16];
  arr1.sort(function(a, b) { //固定写法
      return a - b; //a-b升序 b-a降序
  });
  console.log(arr1);
  ```

  

- #### 获取数组元素索引

  ```js
  //1. indexOf() 数组中查找给定元素的第一个索引 存在返回索引号，不存在返回-1
  var arr = ["red", 8, "red", 2, 3, 4, "hi"];
  console.log(arr.indexOf('red'));
  console.log(arr.indexOf('blue'));
  console.log(arr.indexOf(2));
  
  //2. lastIndexOf() 在数组中的最后一个索引 存在返回索引号，不存在返回-1
  console.log(arr.lastIndexOf('red'));
  console.log(arr.lastIndexOf('blue'));
  console.log(arr.lastIndexOf(2));
  ```

  

- #### 数组去重

  ```js
  var arr = ['c', 'a', 'z', 'a', 'x', 'a', 'x', 'c', 'b'];
  var newArr = [];
  for (var i = 0; i < arr.length; i++) {
      if (newArr.indexOf(arr[i]) === -1) {
          newArr.push(arr[i]);
      }
  }
  console.log(newArr);
  ```

  

- #### 数组转字符串

  ```js
  //1. toString() 
  var arr = [1, 2, 3];
  console.log(arr.toString());
  
  //2. join('分隔符')
  console.log(arr.join('_'));
  ```

  