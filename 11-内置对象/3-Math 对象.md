# Math 对象

- #### 最大值

  ```js
  console.log(Math.max(1, 2, 3));
  console.log(Math.max(-1, -2, -3));
  console.log(Math.max(-1, 2, '小明')); //NaN
  console.log(Math.max()); //-Infinity
  ```

  

- #### 绝对值

  ```js
  console.log(Math.abs(-2));
  console.log(Math.abs(2));
  console.log(Math.abs('-2')); //隐式转换
  ```

  

- #### 取整

  ```js
  //1. 向下取整
  console.log(Math.floor(1.1));
  console.log(Math.floor(1.9));
  
  //2. 向上取整
  console.log(Math.ceil(1.1));
  console.log(Math.ceil(1.9));
  
  //3. 四舍五入
  console.log(Math.round(1.1));
  console.log(Math.round(1.5));
  console.log(Math.round(1.9));
  console.log(Math.round(-1.1)); //-1
  console.log(Math.round(-1.5)); //-1, 往大取
  console.log(Math.round(-1.9)); //-1
  ```

  

- #### 随机数

  ```js
  //random() 返回一个随机小数 [0,1)
  console.log(Math.random());
  
  //返回min~max之间的随机整数
  function getRandomIntInclusive(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min; //含最大值，含最小值 
  }
  console.log(getRandomIntInclusive(1, 10));
  ```

  