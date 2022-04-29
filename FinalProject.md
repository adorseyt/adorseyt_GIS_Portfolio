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

In addition, the project will include a web guide to facilitate the transition of ownership to Hiking Mirdita. It will include a brand package of custom markers, colors, and fonts used as well as reference documentation for modifying the map and creating new maps if needed. In addition to ensuring that the deliverable is viable and adaptable in the long term, this document is in dedication to the sustainable development ethos that provides organizations the resources to in-source work that may otherwise be cost prohibitive.

### Existing Inputs

A major component of this project will be the compilation of disparate resources into a single product. Line layers of the 38 trails have been provided, but will need to be cleaned to remove duplicates, combined in cases where a single trail has been broken into multiple shapes, and cross-referenced with information on the Hiking Mirdita website to connect each trail to its title. Trail elevation journey charts and descriptive statistics are available in separate pdfs; for each of the 38 trails it will be required to reformat these into images that are appropriate for Google Maps pop-ups. 

There are no current spatial files for attractions and accommodations. Instead, I will be leveraging map images created as part of an old slide deck and using a mix of visual analysis on Google Earth and researching region records to identify the correct location. These 43 points will be added manually to the attraction layers. Images (where possible) will be similarly sourced from documentation owned by Hiking Mirdita. Because of the relatively undocumented nature of most of these assets, it is estimated that this process will require creative problem solving and is reflected in the time estimated for this segment of the project.

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

This section outlines at a high-level the way in which I attempted to create the web map. It describes the features of each step and the pitfalls/successes that led me to create a number of options for Hiking Mirdita.

#### Preparation in Google Maps 

I began by downloading the KML layer for the hiking trials. In their original form, there were 64 line layers, some representing a segment of a larger trail. I combined segments to create 37 features, and added a missing hiking trial (SH_MR_08) to create a single "Hiking Trails" layer. 

I then created three new layers for the attractions - history, nature and accommodation. Adding markers to the correct locations turned out to be one of the most difficult aspects of the project. Even with the catalogue and google, it quickly (or not not quickly; after ~6.5 hours) became clear that it would be impossible to pinpoint locations to the precision and accuracy required for a true directional map. This is the first deviation from the intent of the project; instead of a product that could be immediately embedded in the organization's website, I was creating a proof of concept that could be modified once all attractions had been properly geocoded.

I designed custom icons for the attraction points layers using a mix of <a href= "https://www.canva.com/">Canva</a> and <a href="https://www.gimp.org/">GIMP</a> image manipulation platforms. I chose to mark accommodations with the <i>kulla</i>, a residential archtecture style found only in this region. For nature, I made a red poppy as it is the Albanian national flower and locally-revered as a sign of spring. Finally, the history points were marked with a quill and books, to harken back to the works of <a href="https://en.wikipedia.org/wiki/Gjergj_Fishta">Gjergj Fishta</a>, an acclaimed Mirditë poet known throughout Albania. These icons were added to the google maps layer.

Finally, I wanted visitors to be able to have sufficient information about the hikes themselves to plan effectively. I reformatted the elevation journey charts and Hiking Mirdita's existing paper maps and added descriptive statistics as attributes to the trails layer. This allowed me to create a side window popup that appeared when any trail was clicked. 

The final results from this step can be found here: [Buidling the Layers and Icons in Google Maps](/GoogleMyMap.html).

While this was already coming together, I didn't like that I couldn't include a custom base map, so the next step was using the <a href="https://mapstyle.withgoogle.com/">Google Maps Style Wizard</a> to make a custom [base Map](/HikingMirditaMap.html). 

I connected these two elements into a [map with layers](/HikingMirditaMapFULL.html), leveraging the MapStatic API as we had done in Assignment 1. However, because the map was static, all the popup infomation was lost. This did not feel like a finished product in this state.

The next step was to experiment with JavascriptMap API to create a fully-interactive Google map. I worked off of tutorials like <a href="https://www.youtube.com/watch?v=CdDXbvBFXLY">this from Coder Coder</a> to code a map in HTML, CSS, and Javascript to combine the base map, knl layers, and pop-ups into a single product. I was also excited for this as it would allow me to also customize the fonts to use Prata and Poppins, typefaces that appear in Hiking Mirdita's website. While the results are technically [here](/HM_MapIndex.html), what will appear is a blank page. Simply put, I struggled with the implementation; I would need much more time to debug the issues than I had left for this project.

So 20+ hours in, I was still missing a map that had all the elements I wanted: custom base map, image markers, and interactive features that allowed visitors to see trail information as a pop-out. I decided to [recreate the map in Esri](/EsriMap.html). While it has all the features I wanted, this isn't a very viable option for Hiking Mirdita. The reason I had restricted the scope of the project to Google at the offset was to avoid cost-prohibitive barriers to them taking final ownership over the map. Putting it simply, Esri is famously not cheap.
