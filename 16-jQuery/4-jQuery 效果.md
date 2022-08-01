# jQuery 效果

- #### 显示隐藏动画效果

  - ##### show([speed, [easing], [fn]])

    - 参数都可以省略，无动画直接显示
    - speed：三种预定速度之一的字符串（'slow', 'normal', 'fast'）或表示动画时长的毫秒数（如：1000）
    - easing：用来指定切换效果，默认是 swing，可用参数 linear
    - fn：回调函数，在动画完成时执行的函数，每个元素执行一次

  ```js
  $(function() {
      $('button').eq(1).click(function() {
          $('div').hide(1000);
      })
      $('button').eq(0).click(function() {
          $('div').show('fast', function() {
              alert('已显示');
          });
      })
      $('button').eq(2).click(function() {
          $('div').toggle(500);
      })
  })
  ```

  

- #### 滑动动画效果

  ```js
  // 参数与显示隐藏动画效果的参数一摸一样
  $(function() {
      $('button').eq(0).click(function() {
          $('div').slideDown();
      })
      $('button').eq(1).click(function() {
          $('div').slideUp();
      })
      $('button').eq(2).click(function() {
          $('div').slideToggle();
      })
  })
  ```

  

- #### 事件切换

  - ##### hover([over,]out)

    - over：鼠标移到元素上时触发的函数（相当于mouseover）
    - out：鼠标移出元素时触发的函数（相当于mouseleave）

  ```js
  $(function() {
      // $('.nav>li').hover(function() {
      //     $(this).children('ul').slideDown(200);
      // }, function() {
      //     $(this).children('ul').slideUp(200);
      // });
    
      //上面的简写形式
      // 如果hover中只写一个函数，那么鼠标经过和鼠标离开都会触发这个函数
      $('.nav>li').hover(function() {
          $(this).children('ul').slideToggle();
      });
  })
  ```

  

- #### 停止动画排队

  ```js
  $(function() {
      $('.nav>li').hover(function() {
          $(this).children('ul').stop().slideToggle();
      });
  })
  ```

  

- #### 淡入淡出动画效果

  ```html
  <button>淡入效果fadeIn</button>
  <button>淡出效果fadeOut</button>
  <button>淡入淡出切换fadeToggle</button>
  <button>修改透明度fadeTo</button>
  <div></div>
  <script>
      // 前三个方法的参数同显示隐藏
    
      // fadeTo([speed],opacity,[easing],[fn])
      // opacity 透明度 取值范围0-1（必写）
      // speed 必写
      $(function() {
          $('button').eq(0).click(function() {
              $('div').fadeIn();
          })
          $('button').eq(1).click(function() {
              $('div').fadeOut();
          })
          $('button').eq(2).click(function() {
              $('div').fadeToggle();
          })
          $('button').eq(3).click(function() {
              $('div').fadeTo(1000, 0.5);
          })
      })
  ```

  

- #### 自定义动画

  - ##### animate(params, [speed], [easing], [fn])

  - params 想要更改的样式属性，以对象的形式传递，必须写。属性名可以不带引号，如果是复合属性则必须采用驼峰命名法

  ```js
  $(function() {
      $('button').click(function() {
          $('div').animate({
              left: 600,
              top: 300,
              opacity: 0.4
          }, 500)
      })
  })
  ```

  