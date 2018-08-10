Chart.js
===
> [Demo Link](https://diuer.github.io/test-Chart.js/)
> [Source Code](https://github.com/Diuer/test-Chart.js)
## Step1 使用Chart.js
1. GitHub載最新Chart.js [連結](https://github.com/chartjs/Chart.js/releases/tag/v2.7.2)
2. 使用Chart.js CDN [連結](https://cdnjs.com/libraries/Chart.js)
```
// index.html
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.2/Chart.js"></script>
```

## Step2 建立Chart
```
// index.html
<canvas id="myChart" width="400" height="400"></canvas>
```
```
//index.js
var ctx = document.getElementById("myChart");
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255,99,132,1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero:true
                }
            }]
        }
    }
});
```

## Step3 客制化圖表
1. 圖表的種類 修改index.js中的type: 'bar'
```
//長條圖
type: 'bar'
//折線圖
type: 'line'
//雷達圖
type: 'radar'
//派圖與甜甜圈圖
type: 'pie'
type: 'doughnut'
…
…
```
2. 圖表邊框 修改index.js
```
//加在 datasets 裡
datasets:[{
    data: [12, 19, 3, 5, 2, 3],
    borderWidth: 1, //邊框粗細
    borderColor: '#000000', //邊框顏色
    hoverBorderWidth: 3, //滑鼠移上去時的邊框粗細
    hoverBorderColor: '#000000' //滑鼠移上去時的邊框顏色
}]
```
> 注意hoverBorderWidth等的大小寫為固定的

3. 圖表字體設置 修改index.js
```
//加在 new Chart之前
Chart.defaults.global.defaultFontFamily='微軟正黑體'; //字體
Chart.defaults.global.defaultFontSize=18; //字的大小
Chart.defaults.global.defaultFontColor='#000000'; //字的顏色
```
4. 設置圖表基本顯示 修改index.js
```
//加在 datasets 後
options: {
    title: {
        display: true, //標題顯示與否
        text: 'This is a Table\'s title', //標題內容
        fontSize: 25 //標題大小
    },
    legend: {
        position: 'right' //圖例位置
    }
```



## 資料來源
1. http://www.chartjs.org/docs/latest/
2. https://www.youtube.com/watch?v=sE08f4iuOhA
