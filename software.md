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

<canvas id="myChart" style="width:100%;max-width:700px"></canvas>

<script>
var xyValues = [
  {x:50, y:7},
  {x:60, y:8},
  {x:70, y:8},
  {x:80, y:9},
  {x:90, y:9},
  {x:100, y:9},
  {x:110, y:10},
  {x:120, y:11},
  {x:130, y:14},
  {x:140, y:14},
  {x:150, y:15}
];

new Chart("myChart", {
  type: "scatter",
  data: {
    datasets: [{
      pointRadius: 4,
      pointBackgroundColor: "rgb(0,0,255)",
      data: xyValues
    }]
  },
  options: 
  {
        layout:
            padding: 20
        }
         {
    legend: {display: false},
           {
   scales: {
      xAxes: [{ticks: {min: 40, max:160}}],
      yAxes: [{ticks: {min: 6, max:16}}],
    }
  }
});
</script>

