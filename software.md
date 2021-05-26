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
var xValues = [50,60,70,80,90,100,110,120,130,140,150];
var yValues = [7,8,8,9,9,9,10,11,14,14,15];

new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      fill: false,
      lineTension: 0,
      backgroundColor: "rgba(0,0,255,1.0)",
      borderColor: "rgba(0,0,255,0.1)",
      data: yValues
    }]
  },
  options: {
    legend: {display: true},
    scales: {
      yAxes: [{ticks: {min: 6, max:16}}],
    }
    padding: {
                left: 50
  }
});
</script>
