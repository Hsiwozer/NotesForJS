# jQuery 事件

1. #### 事件注册

   ```js
   $(function() {
       // 单个事件注册
       $('div').click(function() {
           $(this).css('background', 'pink');
       })
       $('div').mouseover(function() {
           $(this).css('background', 'skyblue');
       })
   })
   ```

   

2. #### 事件处理on绑定事件

   ```js
   $(function() {
       // 两种写法
       // $('div').on({
       //     mouseenter: function() {
       //         $(this).css('background', 'pink');
       //     },
       //     click: function() {
       //         $(this).css('background', 'skyblue');
       //     },
       //     mouseleave: function() {
       //         $(this).css('background', 'purple');
       //     }
       // });
     
       $('div').on('mouseenter mouseleave', function() {
           $(this).toggleClass('current');
       })
   })
   ```

   

3. #### on实现事件委派

   ```html
   <ul>
       <li>on实现事件委派</li>
       <li>on实现事件委派</li>
       <li>on实现事件委派</li>
       <li>on实现事件委派</li>
       <li>on实现事件委派</li>
   </ul>
   <ol>
   </ol>
   <script>
       $(function() {
           // 给ul添加了点击事件，但是触发对象是li
           $('ul').on('click', 'li', function() {
               alert(11);
           });
           // on可以给未来动态创建的元素绑定事件
           $('ol').on('click', 'li', function() {
               alert(33);
           });
           var li = $('<li>我是后来创建的li</li>');
           $('ol').append(li);
       })
   </script>
   ```

   

4. #### 事件处理off解绑事件

   ```html
   <div></div>
   <ul>
       <li>off解除事件委托</li>
       <li>off解除事件委托</li>
       <li>off解除事件委托</li>
   </ul>
   <script>
       $(function() {
           $('div').click(function() {
               $(this).css('background', 'pink');
           })
           $('div').mouseover(function() {
               $(this).css('background', 'skyblue');
           })
           // 若括号内为空，则解绑所有事件
           // $('div').off();
           $('div').off('click');
           // off解除事件委托
           $('ul').on('click', 'li', function() {
               alert(11);
           })
           $('ul').off('click', 'li');
       })
   </script>
   ```

   

5. #### 事件绑定one只触发一次

   ```html
   <p>我是p</p>
   <script>
       $(function() {
           $('p').one('click', function() {
               alert(11);
           });
       })
   </script>
   ```

   

6. #### 自动触发事件

   ```js
   $(function() {
       $('div').on('click', function() {
           alert(11);
       });
       // 1. element.click();      会触发元素的默认行为
       // $('div').click();
     
       // 2. element.trigger() 方法        会触发元素的默认行为
       // $('div').trigger('click');
     
       // 3. element.triggerHandler() 方法     不会触发元素的默认行为(如文本框的光标闪烁)
       $('div').triggerHandler('click');
   })
   ```

   

7. #### 事件对象

   ```js
   $(function() {
       $(document).on('click', function() {
           console.log('点击了document');
       })
       $('div').on('click', function(e) {
           // console.log(e);
           console.log('点击了div');
           e.stopPropagation(); //阻止冒泡
       })
   })
   ```

   