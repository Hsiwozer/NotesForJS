# String 对象

- #### 基本包装类

  ```js
  var str = 'lihua';
  console.log(str.length);
  
  //基本包装类：把简单数据类型包装成了复杂数据类型
  //(1) 把简单数据类型包装成了复杂数据类型
  var temp = new String('lihua');
  //(2) 把临时变量的值给str
  str = temp;
  //(3) 销毁临时变量temp
  temp = null;
  ```

  

- #### 根据字符返回位置

  ```js
  var str = '今天天气真好,元气满满';
  
  //1. indexOf('要查找的字符', [起始位置])
  console.log(str.indexOf('你'));
  console.log(str.indexOf('气', 4));
  
  //2. lastIndexOf()
  console.log(str.lastIndexOf('气'));
  ```

  

- #### 根据位置返回字符

  ```js
  var str = '今天天气真好,元气满满';
  
  //1. charAt(index) 返回指定位置的字符
  console.log(str.charAt(3));
  
  //2. charCodeAt(index) 获取指定位置处字符的ASCII码
  console.log(str.charCodeAt(3));
  
  //3. str[index] 获取指定位置的字符 H5新增
  console.log(str[3]);
  ```

  

- #### 拼接字符串

  ```js
  // 等效于 +
  var str = 'Good';
  console.log(str.concat('ness'));
  ```

  

- #### 截取字符串

  ```js
  var str = '今天天气真好,元气满满
  
  //1. substr(start, length)
  console.log(str.substr(2, 2));
  
  //2. slice(start, end)
  console.log(str.substr(2, 4));
  
  //3. substring(start, end)
  console.log(str.substr(2, 2));
  ```

  

- #### 替换字符

  ```js
  // 只会替换第一个字符
  var str = '今天天气真好,元气满满';
  console.log(str.replace('今天', '昨天'));
  ```

  

- #### 字符串转数组

  ```js
  // split('分隔符')
  var str = 'red, pink, blue';
  console.log(str.split(','));
  ```

  