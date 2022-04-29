## Final Project: Custom Web Map for Hiking Mirdita

### Introduction

For this assignment, we were tasked with choosing an organization and building a custom product that leverages the GIS material we were exposed to throughout the course. We had the option of performing spatial analysis, such as understand factors to predict outcomes or assessing suitability to inform the location of new infrastructure, but we were also allowed to expand upon the map design curriculum presented in Assignment 1. 

In choosing the topic of this project, my mind went repeatedly to an organization I worked with in Albania. In that capacity, I worked with a team to document and highlight regional assets to promote eco-tourism and invite visitors. The organization's adventure tourism arm, Hiking Mirdita, sought to create outdoor experiences by creating hiking trails throughout the region. At the time of my leaving, they had mapped 38 hiking trails and created a catalog of local attractions.

This project was an opportunity for me to take these resources to their logical conclusion; an interactive map on the organization's web site that allowed visitors to plan their trips. This page presents the original idea, process workflow, and a discussion of the final results.

### About the Client

Hiking Mirdita is a non-profit organization built in partnership with the Municipal Department of Tourism to facilitate eco-tourism opportunities in the Mirdite region of Albania. It is headed by Infokulla, a museum and economic development organization aimed at sharing the natural wonder and cultural heritage of this area. 

Mirdita is part of the nation’s northern foothills, nestled against Mount Munella. The region’s rich history spans millennia, with prehistoric cave carvings, intact Roman roads, and medieval churches dotting the landscape.

Established in 2019, Hiking Mirdita has made great strides in establishing the region as a tourist destination for outdoor adventure. Together with volunteers and local constituents, they have mapped and developed 38 traditional shepards’ paths into hiking trails that meet international standards. Moving forward, the organization is seeking to promote economic development by connecting hikers to locally-owned attractions, restaurants, and bed & breakfasts (known as bujtina). It has partnered with families to convert the region’s kulla style houses along hiking trails into destinations where visitors can experience traditional Mirdite food and culture.

### Project Summary

This project will create an interactive Google Map that allows hikers to plan their trips around the Mirditë region of Albania. It will consist of 4 layers: hiking trails, natural attractions, historical attractions, and accommodations, that will be presented on a custom base map designed to the organization’s green and white brand standards. When clicked, each trail will display an elevation journey chart as well as descriptive statistics like distance, difficulty, and estimated duration. The point layers will have custom markers and allow users to see the name and description of the attraction, as well as photos when available. 

In addition, the project will include a web guide to facilitate the transition of ownership to Hiking Mirdita. It will include a brand package of custom markers, colors, and fonts used as well as reference documentation for modifying the map and creating new maps if needed. In addition to ensuring that the deliverable is viable and adaptable in the long term, this document is in dedication to the sustainable development ethos that provides organizations the resources to insource work that may otherwise be cost-prohibitive.

### Measures of Success & Final Deliverables
I created a list of features that should be included in the final product. These were used as a metric to evalute if the project was successful. I planned for the deliverables to include:

<b>Google Map with:</b>
- Custom base map
- Trial line layer with 38 hiking trails
- History point layer with 17 points marked with custom symbology
- Nature point layer with 17 points marked with custom symbology
- Accommodation point layer with 8 points marked with custom symbology
- Pop-outs with title and descriptive statistics image for 38 hiking trails
- Pop-outs with title and images (where possible) for 42 attraction points.

<b>Web Guide with:</b>
- Zipped folder of custom symbology
- Brand guide with colors, font styles, and map option selections used
- Step by step instructions for embedding the map into a website
- Step by step instructions for opening and modifying the map
- Step by step instructions for creating a new map
-Meta documentation for use of the guide

### Work Process

[Custom Layer Map](/GoogleMyMap.html)
<p>Starting map used to create the layers, custom icons, and formatted pop-outs with trail images. Does not contain the custom base map.</p>

[Base Map](/HikingMirditaMap.html)
<p>Custom base map without layers.</p>

[Map with layers](/HikingMirditaMapFULL.html)
<p>Custom base map with the layers. Does not contain custom icons and is static (without pop-outs)</p>

[Interactive Map](/HM_MapIndex.html)
<p>Attempt to have all elements using a javascript API style map</p>

[Esri Map](/EsriMap.html)
<p>ArcGIS version of the map that contains a custom base map, custom markers, and pop-outs, and images formatted for the trails.</p>
