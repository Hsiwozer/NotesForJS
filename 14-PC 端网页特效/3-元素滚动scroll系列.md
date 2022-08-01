# 元素滚动scroll系列

- #### scrollWidth 和 scrollHeight

  - ##### <font color="red">scrollWidth</font>

    - ###### 返回自身实际的<font color="red">宽度</font>，不包含边框但包含padding，返回数值不带单位

  - ##### <font color="red">scrollHeight</font>

    - ###### 返回自身实际的<font color="red">高度</font>，不包含边框但包含padding，返回数值不带单位

  ```html
  <div>我是内容</div>
  <script>
      var div = document.querySelector('div');
      console.log(div.scrollWidth);
      console.log(div.scrollHeight);
  </script>
  ```

  

- #### scrollTop 和 scrollLeft

  - ##### <font color="red">scrollTop</font>

    - ###### 返回被卷去的<font color="red">上侧</font>距离，返回数值不带单位

  - ##### <font color="red">scrollLeft</font>

    - ###### 返回被卷去的<font color="red">左侧</font>距离，返回数值不带单位

  ```html
  <div>我是内容</div>
  <script>
      var div = document.querySelector('div');
      console.log(div.scrollTop);
      console.log(div.scrollLeft);
  </script>
  ```

  

- #### onScroll 事件

  ```html
  <div>我是内容</div>
  <script>
      var div = document.querySelector('div');
      div.addEventListener('scroll', function() {
          console.log(div.scrollTop);
      });
  </script>
  ```