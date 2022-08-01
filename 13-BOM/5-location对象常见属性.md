# location对象

- #### 常见属性

  - #### <font color="red">**location.href**</font> 获取或设置整个URL

  - <font color="red">**location.host**</font> 返回主机（域名）

  - <font color="red">**location.port**</font> 返回端口号

  - <font color="red">**location.pathname**</font> 返回路径

  - <font color="red">**location.search**</font> 返回参数

  - <font color="red">**location.hash**</font> 返回片段 #后面的内容 常用于链接锚点

  ##### 案例：

  ###### 自动跳转

  ```html
  <div></div>
  <script>
      var div = document.querySelector('div');
      var time = 5;
      fn();
      setInterval(fn, 1000);
    
      function fn() {
          if (time == 0) {
              location.href = 'http://www.itcast.cn';
          }
          div.innerHTML = time + '秒后自动跳转至首页';
          time--;
      }
  </script>
  ```

- #### 常见方法

  - <font color="red">**location.assign()**</font> 跟href一样，可以跳转页面（重定向页面）

    ```js
    btn.addEventListener('click', function() {
        location.assign('http://www.itcast.cn');
    });
    ```

    

  - <font color="red">**location.replace()**</font> 替换当前页面，因为不记录历史，所以不能后退

    ```js
    btn.addEventListener('click', function() {
        location.replace('http://www.itcast.cn');
    });
    ```

    

  - <font color="red">**location.reload()**</font> 重新加载页面，相当于刷新按钮或者 f5 ，如果参数为true则强制刷新

    ```js
    btn.addEventListener('click', function() {
        location.reload();
    });
    ```

    

​	

