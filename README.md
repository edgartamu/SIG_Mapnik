# SIG_Mapnik
Proyecto para poder renderizar mapas desde una base de datos de postgis


## World Boundaries
Descargar los datos para la configuración de World Boundaries:
<pre>
   wget https://planet.openstreetmap.org/historical-shapefiles/world_boundaries-spherical.tgz
   wget https://planet.openstreetmap.org/historical-shapefiles/processed_p.tar.bz2
   wget https://planet.openstreetmap.org/historical-shapefiles/shoreline_300.tar.bz2
   wget http://www.naturalearthdata.com/http//www.naturalearthdata.com/download/10m/cultural/ne_10m_populated_places.zip
   wget http://www.naturalearthdata.com/http//www.naturalearthdata.com/download/110m/cultural/ne_110m_admin_0_boundary_lines_land.zip
</pre>
Descomprimir los archivos dentro del repositorio en una carpeta que llamaremos "world_boundaries":
<pre>
   tar xvzf world_boundaries-spherical.tgz
   tar xvjf processed_p.tar.bz2 -C world_boundaries
   tar xvjf shoreline_300.tar.bz2 -C world_boundaries
   unzip ne_10m-populated-places.zip -d world_boundaries
   unzip ne_110m-admin-0-boundary-lines.zip -d world_boundaries
   cd world_boundaries
   ln -s ne_110m_admin_0_boundary_lines_land.shp 110m_admin_0_boundary_lines_land.shp
   ln -s ne_110m_admin_0_boundary_lines_land.dbf 110m_admin_0_boundary_lines_land.dbf
</pre>
