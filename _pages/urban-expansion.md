---
title: "Urban Spatial Expansion — Bahir Dar"
permalink: /urban-expansion/
classes: wide
---

<p>Land cover classification of Bahir Dar (2024) using Random Forest on Sentinel imagery in Google Earth Engine. Toggle the opacity slider to compare against real satellite imagery below.</p>

<div id="expansion-map" style="width:100%; height:600px; border-radius:10px;"></div>

<div style="margin-top:1em; display:flex; align-items:center; gap:1em;">
  <label for="opacity-slider">Classification opacity:</label>
  <input type="range" id="opacity-slider" min="0" max="1" step="0.05" value="0.75" style="width:200px;">
</div>

<div style="margin-top:1em; display:flex; flex-wrap:wrap; gap:1.5em; font-size:0.9em;">
  <span><span style="display:inline-block;width:14px;height:14px;background:#2563eb;border-radius:3px;"></span> Water</span>
  <span><span style="display:inline-block;width:14px;height:14px;background:#228b22;border-radius:3px;"></span> Built-up</span>
  <span><span style="display:inline-block;width:14px;height:14px;background:#c81e1e;border-radius:3px;"></span> Vegetation</span>
  <span><span style="display:inline-block;width:14px;height:14px;background:#c29a5c;border-radius:3px;"></span> Cropland</span>
  <span><span style="display:inline-block;width:14px;height:14px;background:#f0c828;border-radius:3px;"></span> Other / Wetland</span>
</div>

<p style="margin-top:1.5em;"><a href="https://code.earthengine.google.com/1bf7b707ab93df292f7973ea19eaedd6" target="_blank">View GEE Script (requires Google Earth Engine account) ↗</a></p>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.css" />
<script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.js"></script>
<script>
  var map = L.map('expansion-map').setView([11.5927, 37.3682], 13);

  L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}', {
    attribution: 'Esri World Imagery',
    maxZoom: 18
  }).addTo(map);

  var bounds = [[11.547303988185977, 37.27945547026126], [11.638123663410461, 37.45705240193169]];
  var overlay = L.imageOverlay('/assets/images/bdr_classified_2024.png', bounds, {opacity: 0.75}).addTo(map);

  map.fitBounds(bounds);

  document.getElementById('opacity-slider').addEventListener('input', function(e) {
    overlay.setOpacity(e.target.value);
  });
</script>
