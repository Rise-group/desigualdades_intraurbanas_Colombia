# Datos geográficos

## Descripción y fuente de los datos
Shapefiles de municipios y manzanas censales obtenidos de la versión 2018 del Marco Geoestadístico Nacional del DANE (niveles geográficos Municipio y Manzana Censal respectivamente). 

URL:
https://geoportal.dane.gov.co/servicios/descarga-y-metadatos/descarga-mgn-marco-geoestadistico-nacional/

## Puesta a punto de geodatos
Los polígonos de municipios se procesaron con la librería `rmapshaper` en R para simplificar su geometría y hacer su despliegue más rápido. Se usó la función **ms_simplify()** y se conservó el 1% de los vértices. El conjunto de datos de municipios simplificados se usó para crear los límites de regiones para que coincidan perfectamente en el espacio. Los polígonos de regiones se crearon a partir de los polígonos de departamentos, siguiendo la delimitación de regiones propuesta por el Departamento Nacional de Planeación de Colombia en el Plan de Desarrollo 2018-2022 y los siguientes códigos:

- 1, Pacífico: Cauca (19), Chocó (27), Nariño (52) y Valle del Cauca (76).  
- 2, Eje cafetero y Antioquia: Caldas (17), Quindío (63), Risaralda (66) y Antioquia (05).  
- 3, Caribe: Atlántico (08), Magdalena (47), Bolívar (13), Córdoba (23), Sucre (70), Cesar (20) y La Guajira (44).  
- 4, Central: Boyacá (15), Cundinamarca (25), Tolima (73), Huila (41) y el Distrito Capital de Bogotá (11).  
- 5, Santanderes: Santander (68) y Norte de Santander (54).  
- 6, Llanos y Orinoquía: Arauca (81), Casanare (85), Meta (50) y Vichada (99).  
- 7, Amazonía: Amazonas (91), Caquetá (18), Guainía (94), Guaviare (95), Putumayo (86) y Vaupés (97).  
- 8, Seaflower: San Andrés, Providencia y Santa Catalina (88).  

## Nombres de archivos
Conjuntos de geodatos en formato shapefile (e identificadores únicos) para unir con los datos tabulares:
- MANZANAS_COL (MANZ_CCNCT)
- MUNICIPIOS_COL (MPIO_CCNCT)
- REGIONES_COL (REG_CCDG)

## Sistema de referencia de coordenadas - SRC:
El sistema de referencia de coordenadas (src) de estos conjuntos de datos es WGS 1984, EPSG:4326.

Este repositorio se terminó de preparar en 2020-10-23.
© Grupo RiSE, Universidad EAFIT, 2020.

### Citación en formato Bibtext:
@misc{urbanIneq2020,
  author = {RiSE-group},
  title = { Intra-urban inequalities in Colombia },
  year = {2020},
  note = {data retrieved from RiSE-group, 
          \url{https://github.com/Rise-group/desigualdades_intraurbanas_Colombia}},
}

