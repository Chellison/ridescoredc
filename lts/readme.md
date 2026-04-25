# Level of Traffic Stress Implementation

This notebook implements the [Level of Traffic Stress](https://peterfurth.sites.northeastern.edu/2014/05/21/criteria-for-level-of-traffic-stress/) model. Specifically, the [2022 edition](https://bpb-us-e1.wpmucdn.com/sites.northeastern.edu/dist/e/618/files/2014/05/LTS-Tables-v2.2.pdf) though there is more background in the [original model](https://peterfurth.sites.northeastern.edu/level-of-traffic-stress/).

In short, this quantifies how stressful or comfortable a road is to bike on.
* Level 1: Cyclists are not in contact with traffic (except for slow, low volume traffic); comfortable for all level of cycling abilities (including children).
* Level 2: Cyclists have their own space and intersections are easy to navigate; comfortable for adult cyclists.
* Level 3: Cyclists interact with some moderate/multi-lane traffic or close to higher-speed traffic; acceptable for 'enthused and confident' cyclists.
* Level 4: Cyclists interact with or are near high-speed traffic; acceptable for 'strong and fearless' cyclists.

The first step was find correspondence between the descriptions and the available [DC road data](https://opendata.dc.gov/datasets/DCGIS::roadway-block/about).

Then, the LTS descriptions are translated into criteria that can be extracted from the data (see LTS.xlsx)

Lastly, the new per road segment data is added to the postgis database and the function and html files are updated to incorporate the LTS. See 'mvp_map' folder.