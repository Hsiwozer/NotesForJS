# jQuery 概述

1. #### jQuery的基本使用及入口函数

   ```js
   // 1. 等着页面DOM加载完毕再去执行js代码
   // $(document).ready(function() {
   //     $('div').hide();
   // })
   
   // 2. 等着页面DOM加载完毕再去执行js代码（写法更简单）
   $(function() {
       $('div').hide();
   })
   ```

   

2. #### jQuery的顶级对象 $

   ```js
   // 1. $ 是jQuery的别称
   $(function() {
       alert('11');
       $('div').hide();
   })
   // jQuery(function() {
   //     alert('11');
   //     jQuery('div').hide();
   // })
   
   // 2. $ 是jQuery的顶级对象
   ```

   

3. #### DOM对象和jQuery对象

   ```js
   // 1. DOM对象：用原生js获取过来的对象
   var myDiv = document.querySelector('div');
   console.log(div);
   
   // 2. jQuery对象：用jQuery方式获取过来的对象。 本质：通过$把DOM元素进行了包装
   $('div'); //$('div')是一个jQuery对象
   
   // 3. jQuery对象只能使用jQuery方法，DOM对象则使用原生的JavaScript属性和方法
   ```

   

4. #### DOM对象和jQuery对象相互转换

   ```js
   // 1. DOM对象转换为jQuery对象
   // (1) 直接获取视频得到的就是jQuery对象
   $('video');
   // (2) 通过使用原生js获取过来的DOM对象
   var myvideo = document.querySelector('video');
   $(myvideo);
   
   // 2. jQuery对象转换为DOM对象
   $('video')[0] //中括号中为index索引，当前只有一个video元素，所以index为0
   $('video').get(0)
   ```

   