# jQuery 属性操作

- #### 获取元素固有属性prop

  ```html
  <a href="https://wht.im/" title="链接">万花筒</a>
  <script>
      $(function() {
          // 获取属性值
          console.log($('a').prop('href'));
          // 设置属性值
          $('a').prop('title', '万花筒');
      })
  </script>
  ```

  

- #### 获取元素自定义属性值attr

  ```html
  <div index="1"></div>
  <script>
      $(function() {
          // 获取属性值
          console.log($('div').attr('index'));
          // 设置属性值
          $('div').attr('index', 3);
          console.log($('div').attr('index'));
      })
  </script>
  ```

  

- #### 数据缓存data

  ```html
  <div index="1"></div>
  <script>
      $(function() {
          // 数据存放在元素的内存里
          $('div').data('uname', 'andy');
          console.log($('div').data('uname'));
      })
  </script>
  ```

  

- #### 内容文本值

  ```html
  <div>
      <span>我是内容</span>
  </div>
  <input type="text" value="请输入内容">
  <script>
      $(function() {
          // 1. 获取设置元素内容
          // console.log($('div').html());
          // console.log($('span').html());
          // $('div').html('123');
        
          // 2. 获取设置元素文本内容
          // console.log($('div').text());
          // console.log($('span').text());
          // $('div').text('123');
        
          // 3. 获取设置表单值
          console.log($('input').val());
          $('input').val('123');
      })
  </script>
  dy>
  ```

  