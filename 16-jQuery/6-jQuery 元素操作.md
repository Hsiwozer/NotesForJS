# jQuery 元素操作

- #### 遍历元素

  ```html
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <script>
      $(function() {
          // 1. each() 方法遍历元素
          var arr = ['red', 'blue', 'orange'];
          $('div').each(function(index, domEle) {
              // 第一个元素是索引号，可以自己指定名称
              // 第二个参数是DOM元素对象，使用jQuery方法需要先转换为jQuery元素对象$(domEle)
              $(domEle).css('color', arr[index])
          })
        
          // 2. $.each() 方法遍历元素 主要用于遍历数据，处理数据
          // 遍历数组
          $.each(arr, function(index, domEle) {
                  console.log(index);
                  console.log(domEle);
              })
              // 遍历对象
          $.each({
              name: 'andy',
              age: 18
          }, function(index, domEle) {
              console.log(index);
              console.log(domEle);
          })
      })
  </script>
  ```

  

- #### 创建添加删除元素

  ```html
  <ul>
      <li>原先的li</li>
  </ul>
  <div class="test">我是原先的div</div>
  <script>
      $(function() {
          // 1. 创建元素
          var li = $('<li>后来创建的li</li>');
          var div = $('<div>我是后创建的div</div>')
          
          // 2. 添加元素
          // (1) 内部添加
          // $('ul').append(li);      放到内容的最后面
          $('ul').prepend(li); // 放到内容的最前面
          // (1) 外部添加
          $('.test').before(div);
          // $('.test').after(div);
        
          // 3. 删除元素
          // $('ul').remove();    可以删除匹配的元素
          // $('ul').empty();     删除匹配元素的子节点
          $('ul').html(''); // 删除匹配元素的子节点
      })
  </script>
  ```

  