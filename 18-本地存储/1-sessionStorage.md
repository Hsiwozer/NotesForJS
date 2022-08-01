# sessionStorage

```html
<!-- 生命周期为关闭浏览器窗口 -->
<input type="text">
<button class="set">存储数据</button>
<button class="get">获取数据</button>
<button class="remove">删除数据</button>
<button class="del">清空所有数据</button>

<script src="jquery.min.js"></script>
<script>
    $('.set').on('click', function() {
        var val = $('input').val();
        sessionStorage.setItem('uname', val);
    });
    $('.get').on('click', function() {
        sessionStorage.setItem('uname');
    });
    $('.remove').on('click', function() {
        sessionStorage.removeItem('uname');
    });
    $('.del').on('click', function() {
        sessionStorage.clear();
    });
</script>
```

