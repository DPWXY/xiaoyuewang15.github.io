---
layout: single
title: "MISC"
permalink: /MISC/
comments: false
author_profile: true
classes: wide
---

## VLOG
Welcome to my corner of the internet where I share the beauty and wonder of my travels and the enjoyable moments of my daily life! Following and joining me on [Bilibili](https://space.bilibili.com/1742317464) to discover more!
<iframe src="https://space.bilibili.com/1742317464" width="100%" height="512" frameborder="0" allowfullscreen="true"></iframe>

## Travel
Explore the map below to see the places I've visited and hear about the stories behind each journey. Every pin on the map represents a story, a memory, or a piece of advice I have for that location. Zoom in and click on the pins to learn more about my adventures around the world!

<div id="map" style="height: 400px;"></div>  
<script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/leaflet.js"></script>  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/leaflet.css" />  
<script>
var map = L.map('map').setView([20, 0], 2); // Centers the map and sets initial zoom level

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {  
    attribution: 'Map data © <a href="https://openstreetmap.org">OpenStreetMap</a> contributors',  
    maxZoom: 18,  
}).addTo(map);  

// Add places you want to highlight
var places = [
    {"name": "Beijing", "lat": 39.904202, "lon": 116.407394},  
    {"name": "🏠Chongqing", "lat": 29.431585, "lon": 106.912254},
    {"name": "Sichuan", "lat": 30.572815, "lon": 104.066803},
    {"name": "Guangzhou", "lat": 23.129110, "lon": 113.264381}
];
<!-- {"name": "", "lat": , "lon": }, {"name": "", "lat": , "lon": }, -->

places.forEach(function(place) {
    L.marker([place.lat, place.lon]).addTo(map)  
        .bindPopup(place.name); // Popup will show the name when the marker is clicked
});
</script>
