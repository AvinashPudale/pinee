---
layout: default
title: Software
permalink: /software
sequence: 3
features:
  - detail: Record and store the ON and OFF aircon commands with IR receiver
  - detail: Turn on or off the aircon with the IR emitter
  - detail: Measure temperature of another part of the room
  - detail: Go into sleep mode after turning on or off the aircon
---

<section class="section is-small">
  <div class="container">
    <h2 class="title is-1">Web USB</h2>
    <p class="subtitle is-4 is-spaced">Web USB on Chrome browser is used to take in user configuration about how they want to control their aircon.</p>

    <a class="button is-primary" href="{{ site.github.repository_url }}/tree/master/webusb">Download code</a>
    <a class="button is-primary" href="{{ site.url }}/webusb">View demo</a>
    <br>

    {% highlight html %}{%- include_relative webusb/index.html -%}{% endhighlight %}
  </div>
</section>

 <script>
  var getRandomDataArray = function () {
    var dataArray = [];
    for (var i = 0; i < 7; i++) dataArray.push(Math.round(Math.random() * 100));
    return dataArray;
  }

  var chartData = {
    labels : ["January","February","March","April","May","June","July"],
    datasets : [
      {
        label: "My First dataset",
        fillColor : "rgba(220,220,220,0.2)",
        strokeColor : "rgba(220,220,220,1)",
        pointColor : "rgba(220,220,220,1)",
        pointStrokeColor : "#fff",
        pointHighlightFill : "#fff",
        pointHighlightStroke : "rgba(220,220,220,1)",
        data : getRandomDataArray()
      },
      {
        label: "My Second dataset",
        fillColor : "rgba(151,187,205,0.2)",
        strokeColor : "rgba(151,187,205,1)",
        pointColor : "rgba(151,187,205,1)",
        pointStrokeColor : "#fff",
        pointHighlightFill : "#fff",
        pointHighlightStroke : "rgba(151,187,205,1)",
        data : getRandomDataArray()
      }
    ]
  }

  window.onload = function(){
    var chartOptions = { responsive : true };
    var chart = document.getElementById("canvas").getContext("2d");
    window.myBar = new Chart(chart).Line(chartData, chartOptions);
  }
  </script>
