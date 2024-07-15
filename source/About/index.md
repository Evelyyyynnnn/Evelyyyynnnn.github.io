---
title: 👋Hi Guys!
date: 2023-09-11 10:15:38
---

<style>
.button-container {
  text-align: center;
}

.button {
  background-color: black;
  border: 1px solid transparent;
  text-align: center;
  border-radius: 5px;
  padding: 8px 15px;
  display: inline-block;
  font-size: 17px;
  color: white !important;
  text-decoration: none;
  margin: 15px;
}

.button:hover {
  background-color: rgba(0, 100, 200, 0.8);
  color: white;
}

.bubble {
  background-color: black;
  border: 1px solid transparent;
  text-align: center;
  border-radius: 50%;
  padding: 15px; /* 适当增加padding以确保内容居中 */
  display: inline-block;
  font-size: 17px;
  color: white !important;
  text-decoration: none;
  margin: 15px;
  width: 170px; /* 确保宽度和高度相等 */
  height: 60px; /* 确保宽度和高度相等 */
  line-height: 30px; /* 确保文字在圆形中居中 */
}

.bubble:hover {
  background-color: rgba(0, 100, 200, 0.8);
  color: white;
}

.shake-image:hover {
  animation: shake 2s; /* 增加动画持续时间 */
  animation-iteration-count: infinite;
}

.highlight-on-hover:hover {
  color: red; /* 鼠标悬浮时变为红色 */
}

@keyframes shake {
  0% { transform: translate(2px, 2px) rotate(0deg); }
  10% { transform: translate(-2px, -4px) rotate(-2deg); }
  20% { transform: translate(-4px, 0px) rotate(2deg); }
  30% { transform: translate(4px, 4px) rotate(0deg); }
  40% { transform: translate(2px, -2px) rotate(2deg); }
  50% { transform: translate(-2px, 4px) rotate(-2deg); }
  60% { transform: translate(-4px, 2px) rotate(0deg); }
  70% { transform: translate(4px, 2px) rotate(-2deg); }
  80% { transform: translate(-2px, -2px) rotate(2deg); }
  90% { transform: translate(2px, 4px) rotate(0deg); }
  100% { transform: translate(2px, -4px) rotate(-2deg); }
}
</style>

*<small> Back to [Homepage](/index.html) > [Project](/tags/Project/index.html) > [Interview](/tags/Interview/index.html) > [Note](/tags/Note/index.html) > [Post](/About/index.html)</small>*

<div align="center">
  <img src="https://s2.loli.net/2024/06/29/UYbwhLBKqmGaR9D.png" width="380" height="400" class="shake-image"/>  

  <br>
  <br>
  <font size="6">
    <strong> 
        Welcome to this <a href="/index.html">site</a> and have a <a href="mailto:wd275@cornell.edu">coffee chat</a> with me!
    </strong>
  </font>

  <br>
  <br>
  <font size="5">
    <strong>💬Contact Me</strong> 
  </font>

<hr style="border: 1px solid gray;">

<div class="button-container">
  <a href="https://vicky-post-site.vercel.app/" class="button">My Chinese Finance Blog</a>
  <a href="https://viiiikedy-academy.vercel.app/" class="button">My Academic Site</a>
  <a href="https://jekyll-typing-artist.vercel.app/" class="button">My Art Design Website</a>
  <a href="https://korean-book.netlify.app" class="button">My Korean Learning Book</a>
  <a href="https://vicky-youtube-video.netlify.app" class="button">My Video Site</a><br/>
  <a href="mailto:wd275@cornell.edu" class="button">wd275@cornell.edu</a>
  <a href="https://github.com/Viiiikedy" class="button">Github</a>
  <a href="https://www.instagram.com/viii.iiicky/" class="button">Instagram</a>


<br>
<br>

<!-- Map container -->
<div id="map" style="height: 400px; width: 100%;"></div>

<!-- Leaflet CSS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />

<!-- Leaflet JS -->
<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>

<!-- Initialize the map -->
<script>
  // Initialize the map and set its view to New York, USA
  var map = L.map('map').setView([40.7128, -74.0060], 13);

  // Add the OpenStreetMap tiles
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
  }).addTo(map);

  // Add a marker at the center of New York
  var marker = L.marker([40.7128, -74.0060]).addTo(map);

  // Add a popup to the marker
  marker.bindPopup("<b>New York, USA</b>").openPopup();
</script>

</div>

<br/>
I am proficient in opening and closing Bloomberg Terminal, Yahoo Finance API, Github, Excel, PowerPoint, and Word <br/>
before checking and updating them 20 times a day😄.


<div style="text-align: left;">

<br>
<font size="5">
<strong>📝Note</strong> 
</font>
<hr style="border: 1px solid gray;">

- This site is created based on the template of [hexo-book](https://www.hexothemes.com/theme/kaiiiz-hexo-theme-book/)

</div>
<div style="text-align: left;">

- The [self-learning guidance](https://csdiy.wiki/) from PKU

</div>
