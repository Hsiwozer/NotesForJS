# localStorage

```html
<!-- 生命周期永久生效，除非手动删除，否则关闭页面也存在 -->
<!-- 可以多窗口共享（同一浏览器可以共享） -->
<input type="text">
<button class="set">存储数据</button>
<button class="get">获取数据</button>
<button class="remove">删除数据</button>
<button class="del">清空所有数据</button>

<script src="jquery.min.js"></script>
<script>
    $('.set').on('click', function() {
        var val = $('input').val();
        localStorage.setItem('uname', val);
    });
    $('.get').on('click', function() {
        console.log(localStorage.setItem('uname'));
    });
    $('.remove').on('click', function() {
        localStorage.removeItem('uname');
    });
    $('.del').on('click', function() {
        localStorage.clear();
    });
</script>
```

