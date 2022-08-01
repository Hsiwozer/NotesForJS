# 选择Echarts图表

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./js/echarts.min.js"></script>
    <title>选择Echarts图表</title>
    <style>
        .box {
            width: 600px;
            height: 600px;
            background-color: pink;
        }
    </style>
</head>

<body>
    <div class="box"></div>

    <script>
        var myChart = echarts.init(document.querySelector('.box'));
        var option = {
            tooltip: {
                trigger: 'item'
            },
            legend: {
                top: '5%',
                left: 'center'
            },
            series: [{
                name: '访问来源',
                type: 'pie',
                radius: ['40%', '70%'],
                avoidLabelOverlap: false,
                itemStyle: {
                    borderRadius: 10,
                    borderColor: '#fff',
                    borderWidth: 2
                },
                label: {
                    show: false,
                    position: 'center'
                },
                emphasis: {
                    label: {
                        show: true,
                        fontSize: '40',
                        fontWeight: 'bold'
                    }
                },
                labelLine: {
                    show: false
                },
                data: [{
                    value: 1048,
                    name: '搜索引擎'
                }, {
                    value: 735,
                    name: '直接访问'
                }, {
                    value: 580,
                    name: '邮件营销'
                }, {
                    value: 484,
                    name: '联盟广告'
                }, {
                    value: 300,
                    name: '视频广告'
                }]
            }]
        };
        myChart.setOption(option);
    </script>
</body>

</html>
```

