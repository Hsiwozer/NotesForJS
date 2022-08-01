# 元素可视区client系列

- #### clientWidth和clientHeight

  - ##### <font color="red">clientWidth</font>

    - ###### 返回自身包括 padding、内容区的<font color="red">宽度</font>，不含边框，返回数值不带单位

  - ##### <font color="red">clientHeight</font>

    - ###### 返回自身包括 padding、内容区的<font color="red">高度</font>，不含边框，返回数值不带单位

  ```html
  <div></div>
  <script>
      var div = document.querySelector('div');
      console.log(div.clientWidth);
      console.log(div.clientHeight);
  </script>
  ```

  

- #### clientTop和clientLeft

  - ##### <font color="red">clientTop</font>

    - ###### 返回元素<font color="red">上边框</font>的大小

  - ##### <font color="red">clientLeft</font>

    - ###### 返回元素<font color="red">左边框</font>的大小

  ```html
  <div></div>
  <script>
      var div = document.querySelector('div');
      console.log(div.clientTop);
      console.log(div.clientLeft);
  </script>
  ```

  

- #### 立即执行函数

  - 不需要调用，立马能够自己执行的函数
  - **写法：**(function() {})();    或者    (function(){}());
  - 立即执行函数最大的作用就是独立创建了一个作用域,里面的变量都是局部变量，避免了命名冲突问题

  ```js
  (function() {
      console.log(2);
  })();
  
  (function(a, b) {
      console.log(a + b);
  })(1, 2);
  ```

  