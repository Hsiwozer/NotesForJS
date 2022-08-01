# jQuery 选择器

- #### 基本选择器

  - ##### ID选择器

    - ###### <font color="red">$('#id')</font>

    - 获取指定ID的元素

  - ##### 全选选择器

    - ###### <font color="red">$('*')</font>

    - 匹配所有元素

  - ##### 类选择器

    - ###### <font color="red">$('.class')</font>

    - 获取同一类class的元素

  - ##### 标签选择器

    - ###### <font color="red">$('div')</font>

    - 获取同一类标签的所有元素

  - ##### 并集选择器

    - ###### <font color="red">$('div,p,li')</font>

    - 选取多个元素

  - ##### 交集选择器

    - ###### <font color="red">$('li.current')</font>

    - 交集元素

  - ##### 子代选择器

    - ###### <font color="red">$('ul>li')</font>

    - 获得亲儿子元素

  - ##### 后代选择器

    - ###### <font color="red">$('ul li')</font>

    - 获得所有子元素

- #### 隐式迭代

  ```html
  <div>惊不惊喜，意不意外</div>
  <div>惊不惊喜，意不意外</div>
  <div>惊不惊喜，意不意外</div>
  <div>惊不惊喜，意不意外</div>
  <div>惊不惊喜，意不意外</div>
  <ul>
      <li>相同的操作</li>
      <li>相同的操作</li>
      <li>相同的操作</li>
  </ul>
  <script>
      // 1. 获取五个div元素
      // $('div');
    
      // 2. 给五个div设置背景颜色为粉色
      $('div').css('background', 'pink');
    
      // 3. 隐式迭代就是把匹配的所有元素内部进行遍历循环，给每一个元素添加css方法
      $('ul li').css('color', 'orange');
  </script>
  ```

  

- #### 筛选选择器

  - ##### <font color="red">:first</font>

    - $('li:first')
    - 获取第一个li元素

  - ##### <font color="red">:last</font>

    - $('li:last')
    - 获取最后一个li元素

  - ##### <font color="red">:eq(index)</font>

    - $('li:eq(2)')
    - 获取到的li元素中，选择索引号为2的元素，索引号index从0开始

  - ##### <font color="red">:odd</font>

    - $('li:odd')
    - 获取到的li元素中，选择索引号为奇数的元素

  - ##### <font color="red">:even</font>

    - $('li:even')
    - 获取到的li元素中，选择索引号为偶数的元素

- #### 筛选方法

  - ##### <font color="red">parent()</font>

    - $('li').parent();
    - 查找父级（亲爸爸）

  - ##### <font color="red">parents('.one')</font>

    - $('li').parents('.pne');
    - 查找父级（括号中没参数表示查找所有父级，有参数则表示查找该参数名相关的父级）

  - ##### <font color="red">children(selector)</font>

    - $('ul').children('li');
    - 相当于$('ul>li')，最近一级（亲儿子）

  - ##### <font color="red">find(selector)</font>

    - $('ul').find('li');
    - 相当于$('ul li')，后代选择器

  - ##### <font color="red">siblings(selector)</font>

    - $('.first').siblings('li');
    - 查找兄弟节点，不包括自己本身

  - ##### <font color="red">nextAll([expr])</font>

    - $('.first').nextAll();
    - 查找当前元素之后的所有同辈元素

  - ##### <font color="red">prevAll([expr])</font>

    - $('.last').prevtAll();
    - 查找当前元素之前的所有同辈元素

  - ##### <font color="red">hasClass(class)</font>

    - $('div').hasClass('protected');
    - 检查当前的元素是否含有某个特定的类，如果有，则返回true

  - ##### <font color="red">eq(index)</font>

    - $('li').eq(2);
    - 相当于$('li:eq(2)')，index从0开始

- #### 排他思想

  ```html
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <script>
      $(function() {
          // 1. 隐式迭代：给所有按钮都绑定了点击事件
          $('button').click(function() {
              $(this).css('background', 'pink');
              // 2. 隐式迭代：给其他兄弟按钮都去掉css样式
              $(this).siblings().css('background', '');
          });
      })
  </script>
  ```

  

- #### 链式编程

  ```html
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <button>按钮</button>
  <script>
      $(function() {
          $('button').click(function() {
              // $(this).css('color', 'orange');
              // $(this).siblings().css('color', '');
            
              // 链式编程
              $(this).css('color', 'orange').siblings().css('color', '');
          });
      })
  </script>
  ```

  