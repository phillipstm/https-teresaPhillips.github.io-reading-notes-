# JavaScript Canvas
https://www.javascripttutorial.net/web-apis/javascript-canvas/


1 What does the <canvas> allow a developer to acheive?


HTML5 features the <canvas> element that allows you to draw 2D graphics using JavaScript.

The <canvas> element requires at least two attributes: width and height that specify the size of the canvas:

<canvas width="500" height="300" id="canvas"></canvas>



2. What is the importance of the closing `</canvas> tag?

It provides fallback content to display any text between the opening and closing tags in the event canvas isn't supported by the browser.


3. Explain what the getContext() method does.

The <canvas> element features the getContext() method that returns a render context object.

The getContext() takes one argument which is the type of context. For example, you use the "2d" to get a 2D rendering context object, which is an instance of the CanvasRenderingContext2D interface.

The 2D rendering context allows you to draw shapes, text, images, and other objects.

The following example shows how to select the canvas element using the querySelector() method and access the drawing context by calling its getContext() method:

    let canvas = document.querySelector('#canvas');
    let ctx = main.getContext('2d');


### Check for canvas support
When using the <canvas> element, it’s important to check if the browser supports the getContext() method. To do it, you use the following code:

let canvas = document.querySelector('#main');
if(canvas.getContext) {
   let ctx = main.getContext('2d');
}

## Chart.js Documentation
http://www.chartjs.org/docs/


1 What is Chart.js and how it can be brought into your project?

All that's required is the script included in your page along with a single <canvas> node to render the chart.

ex:
<canvas id="myChart" width="400" height="400"></canvas>
<script>
const ctx = document.getElementById('myChart').getContext('2d');
const myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
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
                'rgba(255, 99, 132, 1)',
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
            y: {
                beginAtZero: true
            }
        }
    }
});
</script>



2. List 3 different Chart types you can create using Chart.js.

Bar Chart
Bubble Chart 
Line Chart


## Easily Create Stunning Animated Charts with Chart.js
https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/


1. What are some advantages to displaying data via a chart over a table?

Charts are far better for displaying data visually than tables they are easy to read and display information cleanly.


2. How could Chart.js aid your previously created applications visually?

You would have a way to display your data in a easy to understand format. 


## Bookmark and Review

Drawing Shapes With Canvas  https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes

Applying Style and Colors - Canvas API   https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors

Drawing Text - Canvas API  https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text


### Things I Want to more about

<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <!-- import plugin script -->
        <script src='Chart.min.js'></script>
    </head>
    <body>
        <!-- line chart canvas element -->
        <canvas id="buyers" width="600" height="400"></canvas>
        <!-- pie chart canvas element -->
        <canvas id="countries" width="600" height="400"></canvas>
        <!-- bar chart canvas element -->
        <canvas id="income" width="600" height="400"></canvas>
        <script>
            // line chart data
            var buyerData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                {
                    fillColor : "rgba(172,194,132,0.4)",
                    strokeColor : "#ACC26D",
                    pointColor : "#fff",
                    pointStrokeColor : "#9DB86D",
                    data : [203,156,99,251,305,247]
                }
            ]
            }
            // get line chart canvas
            var buyers = document.getElementById('buyers').getContext('2d');
            // draw line chart
            new Chart(buyers).Line(buyerData);
            // pie chart data
            var pieData = [
                {
                    value: 20,
                    color:"#878BB6"
                },
                {
                    value : 40,
                    color : "#4ACAB4"
                },
                {
                    value : 10,
                    color : "#FF8153"
                },
                {
                    value : 30,
                    color : "#FFEA88"
                }
            ];
            // pie chart options
            var pieOptions = {
                 segmentShowStroke : false,
                 animateScale : true
            }
            // get pie chart canvas
            var countries= document.getElementById("countries").getContext("2d");
            // draw pie chart
            new Chart(countries).Pie(pieData, pieOptions);
            // bar chart data
            var barData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                    {
                        fillColor : "#48A497",
                        strokeColor : "#48A4D1",
                        data : [456,479,324,569,702,600]
                    },
                    {
                        fillColor : "rgba(73,188,170,0.4)",
                        strokeColor : "rgba(72,174,209,0.4)",
                        data : [364,504,605,400,345,320]
                    }
                ]
            }
            // get bar chart canvas
            var income = document.getElementById("income").getContext("2d");
            // draw bar chart
            new Chart(income).Bar(barData);
        </script>
    </body>
</html>

more info rendering paths:
https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D#paths