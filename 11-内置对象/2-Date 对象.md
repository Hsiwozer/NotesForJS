# Date 对象

- #### 格式化年月日星期

  ```js
  var date = new Date();
  console.log(date.getFullYear()); //返回当前日期年份
  console.log(date.getMonth() + 1); //返回当前日期月份 0-11即一月至十二月
  console.log(date.getDate()); //返回当前日期
  console.log(date.getDay()); //返回当前日期星期 0-6即周日至周六
  
  var year = date.getFullYear();
  var month = date.getMonth() + 1;
  var dates = date.getDate();
  var arr = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
  var day = date.getDay();
  console.log('今天是:' + year + '年' + month + '月' + dates + '日' + arr[day]);
  ```

  

- #### 格式化时分秒

  ```js
  var date = new Date();
  var h = date.getHours();
  h = h < 10 ? '0' + h : h;
  var m = date.getMinutes();
  m = m < 10 ? '0' + m : m;
  var s = date.getSeconds();
  s = s < 10 ? '0' + s : s;
  console.log('现在是: ' + h + ':' + m + ':' + s);
  ```

  

- #### 时间戳

  ```js
  //通过Date对象获得总的毫秒数
  
  //1. 通过valueOf()
  var date = new Date();
  console.log(date.valueOf());
  
  //2. 通过getTime()
  console.log(date.getTime());
  
  //3. 简写(最常用)
  var date1 = +new Date(); //+new Date()返回的就是总的毫秒数
  console.log(date1);
  
  //4. H5新增
  console.log(Date.now());
  ```

  

- #### 倒计时

  ```js
  function countDown(time) {
      var nowTime = +new Date(); //当前毫秒数
      var inputTime = +new Date(time); //用户输入的毫秒数
      var times = (inputTime - nowTime) / 1000; //剩余时间总秒数
      var d = parseInt(times / 60 / 60 / 24); //天数
      d = d < 10 ? '0' + d : d;
      var h = parseInt(times / 60 / 60 % 24); //小时
      h = h < 10 ? '0' + h : h;
      var m = parseInt(times / 60 % 60); //分钟
      m = m < 10 ? '0' + m : m;
      var s = parseInt(times % 60); //秒数
      s = s < 10 ? '0' + s : s;
      return d + '天' + h + '时' + m + '分' + s + '秒';
  }
  console.log(countDown('2021-7-15 21:50:00'));
  ```

  