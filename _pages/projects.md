---
title: "Projects"
permalink: /projects/
classes: wide
---

<style>
.proj-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2em;
  margin-bottom: 2em;
}
.proj-card {
  background: #fff;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
.proj-thumb {
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
}
.proj-thumb-placeholder {
  width: 100%;
  height: 200px;
  background: linear-gradient(135deg, #4a5568, #2d3748);
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 1.1em;
  text-align: center;
  padding: 1em;
  box-sizing: border-box;
}
.proj-body {
  padding: 1.2em;
}
.proj-tags {
  font-size: 0.85em;
  color: #888;
  margin-bottom: 0.5em;
}
.proj-links a {
  display: inline-block;
  margin-top: 0.8em;
  margin-right: 0.8em;
  padding: 0.5em 1em;
  background: #2d3748;
  color: #fff !important;
  border-radius: 6px;
  text-decoration: none;
  font-size: 0.9em;
}
</style>

<div class="proj-grid">

  <div class="proj-card">
    <div class="proj-thumb-placeholder">Bahir Dar Atmospheric Watch<br>Sentinel-5P</div>
    <div class="proj-body">
      <div class="proj-tags">Google Earth Engine · Sentinel-5P TROPOMI · JavaScript</div>
      <strong>Bahir Dar Atmospheric Watch</strong>
      <p>Interactive web map of column concentrations of seven trace gases over Bahir Dar, derived from Sentinel-5P TROPOMI data on Google Earth Engine.</p>
      <div class="proj-links">
        <a href="https://abel-tesfaye-geo.github.io/GEE_GAS_DETECTION/" target="_blank">View Live Demo ↗</a>
        <a href="https://github.com/abel-tesfaye-geo/GEE_GAS_DETECTION" target="_blank">View Repository ↗</a>
      </div>
    </div>
  </div>

  <div class="proj-card">
    <div class="proj-thumb-placeholder">Bahir Dar Basemap<br>Field Survey 2018–2020</div>
    <div class="proj-body">
      <div class="proj-tags">Esri File Geodatabase · GIS · Field Survey</div>
      <strong>Bahir Dar Structural Plan Basemap</strong>
      <p>A field-surveyed digital cadastre of Bahir Dar — parcels, roads, waterways, and control points, digitized 2018–2020 and published as a browsable interactive map.</p>
      <div class="proj-links">
        <a href="https://abel-tesfaye-geo.github.io/structural-plan-BDR/" target="_blank">View Live Demo ↗</a>
        <a href="https://github.com/abel-tesfaye-geo/structural-plan-BDR" target="_blank">View Repository ↗</a>
      </div>
    </div>
  </div>

  <div class="proj-card">
    <img class="proj-thumb" src="/assets/images/1788847547225_image.png">
    <div class="proj-body">
      <div class="proj-tags">Agisoft Metashape · DJI Mavic 3E · UAV Photogrammetry</div>
      <strong>UAV 3D Terrain Reconstruction</strong>
      <p>A dense point cloud reconstructed in Agisoft Metashape from DJI Mavic 3E aerial imagery — 91,341 points captured across a structured flight grid, processed into a georeferenced 3D model and orthophoto for terrain and infrastructure visualization on the Bahir Dar City Structural Plan.</p>
    </div>
  </div>

     <div class="proj-card">
     <img class="proj-thumb" src="/assets/images/bdr_classified_2024.png">
     <div class="proj-body">
       <div class="proj-tags">Google Earth Engine · Random Forest · Sentinel Imagery</div>
       <strong>Urban Spatial Expansion & Land Cover Classification, Bahir Dar</strong>
       <p>Applied Google Earth Engine and a Random Forest classifier to model land cover and quantify urban spatial expansion in Bahir Dar City. Findings were presented at a departmental research seminar.</p>
       <div class="proj-links">
         <a href="/urban-expansion/">View Interactive Map ↗</a>
       </div>
     </div>
   </div>

</div>
