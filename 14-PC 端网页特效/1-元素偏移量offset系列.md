# 元素偏移量offset系列

- #### offsetLeft 和 offsetTop

  <font color="blue">**以带有定位的父亲为准，如果有父亲或父亲没有定位，则以body为准**</font>

  - ##### <font color="red">offsetLeft</font>

    - ###### 返回元素相对带有定位父元素<font color="red">左边框</font>的偏移

  - ##### <font color="red">offsetTop</font>

    - ###### 返回元素相对带有定位父元素<font color="red">上边框</font>的偏移

  ```html
  <div class="father">
      <div class="son"></div>
  </div>
  <script>
      var father = document.querySelector('.father');
      var son = document.querySelector('.son');
      console.log(father.offsetTop);
      console.log(father.offsetLeft);
      console.log(son.offsetLeft);
  </script>
  ```

  

- #### offsetWidth 和 offsetHeight

  - ##### <font color="red">offsetWidth</font>

    - ###### 返回自身包括padding、边框、内容区的<font color="red">宽度</font>，返回数值不带单位

  - ##### <font color="red">offsetHeight</font>

    - ###### 返回自身包括padding、边框、内容区的<font color="red">高度</font>，返回数值不带单位

  ```html
  <div class="w"></div>
  <script>
      var w = document.querySelector('.w');
      console.log(w.offsetWidth);
      console.log(w.offsetHeight);
  </script>
  ```

  

- #### <font color="red">offsetParent</font>

  ###### 返回作为该元素<font color="red">带有定位的父级元素</font>，如果父级都没有定位则返回 <font color="red">body</font>

  ```html
  <div class="father">
      <div class="son"></div>
  </div>
  <script>
      var father = document.querySelector('.father');
      var son = document.querySelector('.son');
      
      console.log(son.offsetParent);
      
      console.log(son.parentNode); //返回最近一级的父亲，不管父亲有没有定位
      
      console.log(father.offsetParent);
  </script>
  ```

  

- #### offset 和 style的区别

  - ##### <font color="red">offset</font>

    - 可以得到任意样式表中的样式值
    - 获得的数值没有单位
    - offsetWidth 包含 padding + border + width
    - offsetWidth 等属性是只读属性，只能获取而不能赋值
    - 想要获取元素大小位置，用 offset 更合适

  - ##### <font color="red">style</font>

    - 只能得到行内样式表中的样式值
    - style.width 获得的是带有单位的字符串
    - style.width 获得不包含 padding 和 border 的值
    - style.width 是可读可写属性，可以获取也可以赋值
    - 想要更改元素的值，则需要用 style 改变

- #### 获取鼠标在盒子中的坐标

  ```html
  <div></div>
  <script>
      var div = document.querySelector('div');
      div.addEventListener('mousemove', function(e) {
          var x = e.pageX - this.offsetLeft;
          var y = e.pageY - this.offsetTop;
          div.innerHTML = 'x坐标是：' + x + '; y坐标是：' + y;
      });
  </script>
  ```

  