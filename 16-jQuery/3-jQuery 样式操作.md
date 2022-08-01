# jQuery 样式操作

- #### css方法

  ```js
  $(function() {
      // 1. 参数只写属性名，则返回属性值
      $('div').css('width');
    
      // 2. 参数是属性名，属性值，逗号分隔，是设置一组样式，属性必须加引号，值如果是数字可以不用跟单位和引号
      $('div').css('width', '300px');
    
      // 3. 参数可以是对象形式，方便设置多组样式。属性名和属性值使用冒号隔开，属性可以不加引号。
      $('div').css({
          height: '400px',
          backgroundColor: 'orange'
      });
  })
  ```

  

- #### 操作类

  - ##### 添加类 addClass()

    ```js
    $('div').click(function() {
        $(this).addClass('current');
    });
    ```

    

  - ##### 删除类 removeClass()

    ```js
    $('div').click(function() {
        $(this).removeClass('current');
    });
    ```

    

  - ##### 切换类 toggleClass()

    ```js
    $('div').click(function() {
        $(this).toggleClass('current');
    });
    ```

    