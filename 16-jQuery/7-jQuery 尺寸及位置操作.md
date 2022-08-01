# jQuery 尺寸及位置操作

- #### 尺寸方法

  ```js
  $(function() {
      // 1. width() / height() 获取设置元素 width 和 height 大小
      console.log($('div').width()); // 获取
      $('div').width(300); // 设置
    
      // 2. innerWidth() / innerHeight() 获取设置元素 width 和 height  + padding 大小
      console.log($('div').innerWidth());
    
      // 3. outerWidth() / outerHeight() 获取设置元素 width 和 height  + padding + border 大小
      console.log($('div').outerWidth());
    
      // 4. outerWidth(true) / outerHeight(true) 获取设置元素 width 和 height  + padding + border + margin 大小
      console.log($('div').outerWidth(true));
  })
  ```

  

- #### 位置方法

  ```js
  $(function() {
      // 1. 获取设置距离文档的位置（偏移） offset
      console.log($('.son').offset());
      console.log($('.son').offset().top);
      // $('.son').offset({
      //     top: 200,
      //     left: 200
      // });
    
      // 2. 获取设置带有定位的父级位置（偏移） position  如果没有带有定位的父级，则以文档为准
      // 这个方法只能获取，不能设置偏移
      console.log($('.son').position());
      console.log($('.son').position().top);
  })
  ```

  

- #### 被卷去的头部方法

  ```html
  <div class="back">返回顶部</div>
  <div class="container"></div>
  <script>
      $(function() {
          $(document).scrollTop(100); // 设置
          // 被卷去的头部 scrollTop() / 被卷去的左侧 scrollLeft()
          // 页面滚动事件
          var boxTop = $('.container').offset().top;
          $(window).scroll(function() {
              if ($(document).scrollTop() >= boxTop) {
                  $('.back').stop().fadeIn();
              } else {
                  $('.back').stop().fadeOut();
              }
          });
        
          // 返回顶部
          $('.back').click(function() {
              // $(document).scrollTop(0);
              // animate()方法是针对元素来操作的
              $('body, html').stop().animate({
                  scrollTop: 0
              });
          })
      })
  </script>
  ```

  

