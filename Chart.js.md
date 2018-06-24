Chart.js
===
> [Demo Link](https://codepen.io/diuer/full/WyyqOy)
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


[資料來源](http://www.chartjs.org/docs/latest/)
