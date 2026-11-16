# Sources of all the data here

Every file here keeps the licence of the sources it was made from. Each source, as the app credits it:

## Callisto Galileo/Voyager Global Mosaic 1km

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://astrogeology.usgs.gov/search/map/callisto_galileo_voyager_global_mosaic_1km
- Credit: USGS Astrogeology Science Center; NASA/JPL Galileo SSI and Voyager images
- Page: https://astrogeology.usgs.gov/search/map/callisto_galileo_voyager_global_mosaic_1km
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. Its longitudes, published west-positive, are made east-positive.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `callisto_galileo_voyager`

## Ceres Dawn FC2 HAMO Global DTM 137m

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/ceres_dawn_fc2_hamo_global_dtm_137m
- Credit: German Aerospace Center (DLR): F. Preusker et al. (2016), Dawn team; NASA/JPL-Caltech/UCLA/MPS/DLR/IDA; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/ceres_dawn_fc2_hamo_global_dtm_137m
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC. Its heights, above a sphere of 470 km, are taken with it as Ceres's shape, and the slopes stored are those against the ellipsoid the app draws Ceres as. The rims of its craters are traced from its heights as well (tools/bodies/rims.py): each is kept as a ring of points, the outline drawn when the crater is picked out on the globe; a crater whose rim the heights do not show keeps the circle of the diameter the Gazetteer states.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `ceres_dawn_dtm`

## Ceres Dawn FC Global Mosaic 400m (October 2015)

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/ceres_dawn_fc_global_mosaic_400m
- Credit: NASA/JPL-Caltech/UCLA/MPS/DLR/IDA, Dawn Framing Camera, mosaic by DLR; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/ceres_dawn_fc_global_mosaic_400m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. What Dawn did not see is left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `ceres_dawn_fc`

## Charon New Horizons LORRI MVIC Global Mosaic 300m (July 2017)

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/charon_new_horizons_lorri_mvic_global_mosaic_300m
- Credit: New Horizons Team: NASA/Johns Hopkins University Applied Physics Laboratory/Southwest Research Institute/Lunar and Planetary Institute; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/charon_new_horizons_lorri_mvic_global_mosaic_300m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. What New Horizons did not see is left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `charon_nh_mosaic`

## Black Marble 2016: the Earth at night, without colour, 3 km (13500 × 6750)

- Publisher: NASA Earth Observatory
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NASA Earth Observatory images by Joshua Stevens, using Suomi NPP VIIRS data from Miguel Román, NASA GSFC
- Page: https://science.nasa.gov/earth/earth-observatory/earth-at-night/maps/
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Only the lights' brightness is used: VIIRS's day/night band sees no colour, so the app draws the lights in one warm colour, on the night side only, far brighter than sunlight would let a camera show them. The compositing chose the clearest moonless nights of 2016.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `earth_black_marble_2016`

## The Blue Marble (2002): the clouds, 2048 × 1024

- Publisher: NASA Earth Observatory, NASA Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://science.nasa.gov/earth/earth-observatory/the-blue-marble-true-color-global-imagery-at-1km-resolution/
- Credit: NASA Goddard Space Flight Center: image by Reto Stöckli (clouds), from MODIS on Terra
- Page: https://science.nasa.gov/earth/earth-observatory/the-blue-marble-true-color-global-imagery-at-1km-resolution/
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). The clouds of two days of MODIS's pictures in visible light, and a third day's in thermal infrared over the poles, as the 2002 Blue Marble composited them: a typical day's cover, not any day's weather. Their brightness is taken as how much of the ground they hide, and the app lets the layer drift slowly round the Earth.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `earth_blue_marble_clouds`

## Blue Marble: Next Generation, July 2004: the land and the shallow seas without clouds, 21600 × 10800

- Publisher: NASA Earth Observatory
- Licence: NASA media guidelines
- Terms: https://science.nasa.gov/earth/earth-observatory/blue-marble-next-generation/
- Credit: NASA Earth Observatory: Blue Marble: Next Generation, by Reto Stöckli (NASA Goddard Space Flight Center), from MODIS on Terra
- Page: https://science.nasa.gov/earth/earth-observatory/blue-marble-next-generation/
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). The month's cloud-free composite of MODIS's pictures, as it is: it shows no sea ice, and the open ocean in one flat blue, as the collection makes it. Its latitudes, geodetic on the WGS 84 ellipsoid, are made planetocentric.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `earth_bmng_july`

## ETOPO 2022 Global Relief Model, 60 arc-seconds, ice surface

- Publisher: NOAA National Centers for Environmental Information
- Licence: CC0 1.0 (public domain)
- Terms: https://data.noaa.gov/metaview/page?xml=NOAA/NESDIS/NGDC/MGG/DEM//iso/xml/etopo_2022.xml&view=getDataView&header=none
- Credit: NOAA National Centers for Environmental Information (2022): ETOPO 2022 Global Relief Model, doi:10.25921/fd45-gt74
- Page: https://www.ncei.noaa.gov/products/etopo-global-relief-model
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC. The land's heights above the sea are used; the sea is taken as flat, its floor left out, so that the relief is that of what is seen. Its latitudes, geodetic on the WGS 84 ellipsoid, are made planetocentric.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `earth_etopo_2022`

## Natural Earth 1:10m Physical Vectors: Lakes and Reservoirs

- Publisher: Natural Earth
- Licence: Public domain
- Terms: https://www.naturalearthdata.com/about/terms-of-use/
- Credit: Made with Natural Earth
- Page: https://www.naturalearthdata.com/downloads/10m-physical-vectors/10m-lakes/
- What was done to it: Not a picture: the coastlines and the lakes' shores drawn onto the map's grid, each pixel's share of water taken from 16 points in it, then resampled onto a cube in the Earth's own axes with every level made from the map itself and compressed as EAC. Where the water is, the sea's sheen of sunlight is drawn.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `earth_ne_lakes`

## Natural Earth 1:10m Physical Vectors: Land, version 5.1.1

- Publisher: Natural Earth
- Licence: Public domain
- Terms: https://www.naturalearthdata.com/about/terms-of-use/
- Credit: Made with Natural Earth
- Page: https://www.naturalearthdata.com/downloads/10m-physical-vectors/10m-land/
- What was done to it: Not a picture: the coastlines and the lakes' shores drawn onto the map's grid, each pixel's share of water taken from 16 points in it, then resampled onto a cube in the Earth's own axes with every level made from the map itself and compressed as EAC. Where the water is, the sea's sheen of sunlight is drawn. The same coastlines, simplified to within 0.1 degrees and without the islands smaller than 700 km², are the Earth drawn on the Home screen, its night side shaded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `earth_ne_land`

## Natural Earth 1:10m Physical Vectors: Marine areas (oceans, seas, gulfs, bays, straits)

- Publisher: Natural Earth
- Licence: Public domain
- Terms: https://www.naturalearthdata.com/about/terms-of-use/
- Credit: Made with Natural Earth
- Page: https://www.naturalearthdata.com/downloads/10m-physical-vectors/
- What was done to it: Each name as Natural Earth gives it in English, at the middle of the largest part of its outline or at its point, with a size worked out from the zoom from which Natural Earth labels it.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `earth_ne_marine_names`

## Natural Earth 1:10m Physical Vectors: Elevation points (mountains)

- Publisher: Natural Earth
- Licence: Public domain
- Terms: https://www.naturalearthdata.com/about/terms-of-use/
- Credit: Made with Natural Earth
- Page: https://www.naturalearthdata.com/downloads/10m-physical-vectors/
- What was done to it: Each name as Natural Earth gives it in English, at the middle of the largest part of its outline or at its point, with a size worked out from the zoom from which Natural Earth labels it.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `earth_ne_peaks`

## Natural Earth 1:10m Physical Vectors: Regions (continents, deserts, plains, ranges, islands)

- Publisher: Natural Earth
- Licence: Public domain
- Terms: https://www.naturalearthdata.com/about/terms-of-use/
- Credit: Made with Natural Earth
- Page: https://www.naturalearthdata.com/downloads/10m-physical-vectors/
- What was done to it: Each name as Natural Earth gives it in English, at the middle of the largest part of its outline or at its point, with a size worked out from the zoom from which Natural Earth labels it.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `earth_ne_region_names`

## Enceladus Cassini Global Mosaic 110m (February 2010)

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/enceladus_cassini_global_mosaic_110m
- Credit: Cassini Imaging Team: NASA/JPL/Space Science Institute; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/enceladus_cassini_global_mosaic_110m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. What Cassini did not map is left unpainted and marked as not seen. Its longitudes, published west-positive, are made east-positive.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `enceladus_cassini_iss`

## Europa Voyager - Galileo SSI Global Mosaic 500m

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://astrogeology.usgs.gov/search/map/europa_voyager_galileo_ssi_global_mosaic_500m
- Credit: USGS Astrogeology Science Center (T. Becker; B. Archinal, T. Colvin, M. Davies, A. Gitlin, R. Kirk, L. Weller); NASA/JPL Galileo SSI and Voyager images
- Page: https://astrogeology.usgs.gov/search/map/europa_voyager_galileo_ssi_global_mosaic_500m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. Its longitudes, published west-positive, are made east-positive.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `europa_galileo_voyager`

## Ganymede Voyager - Galileo SSI Global Mosaic 1km

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://astrogeology.usgs.gov/search/map/ganymede_voyager_galileo_ssi_global_mosaic_1km
- Credit: USGS Astrogeology Science Center; NASA/JPL Galileo SSI and Voyager images
- Page: https://astrogeology.usgs.gov/search/map/ganymede_voyager_galileo_ssi_global_mosaic_1km
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour: the USGS's colour mosaic of Ganymede takes its red from 991 nm and was enhanced, so its monochrome one is used. Its longitudes, published west-positive, are made east-positive.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `ganymede_galileo_voyager`

## Gazetteer of Planetary Nomenclature: the named features of Callisto, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_callisto`

## Gazetteer of Planetary Nomenclature: the named features of Ceres, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_ceres`

## Gazetteer of Planetary Nomenclature: the named features of Charon, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_charon`

## Gazetteer of Planetary Nomenclature: the named features of Enceladus, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_enceladus`

## Gazetteer of Planetary Nomenclature: the named features of Europa, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_europa`

## Gazetteer of Planetary Nomenclature: the named features of Ganymede, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_ganymede`

## Gazetteer of Planetary Nomenclature: the named features of Io, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_io`

## Gazetteer of Planetary Nomenclature: the named features of Mars, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_mars`

## Gazetteer of Planetary Nomenclature: the named features of Mercury, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_mercury`

## Gazetteer of Planetary Nomenclature: the named features of the Moon, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_moon`

## Gazetteer of Planetary Nomenclature: the named features of Pluto, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_pluto`

## Gazetteer of Planetary Nomenclature: the named features of Titan, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_titan`

## Gazetteer of Planetary Nomenclature: the named features of Triton, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_triton`

## Gazetteer of Planetary Nomenclature: the named features of Venus, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_venus`

## Gazetteer of Planetary Nomenclature: the named features of Vesta, as points (shapefile)

- Publisher: IAU Working Group for Planetary System Nomenclature (WGPSN); USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://planetarynames.wr.usgs.gov/Page/FAQ
- Credit: International Astronomical Union Working Group for Planetary System Nomenclature, Gazetteer of Planetary Nomenclature, https://planetarynames.wr.usgs.gov/ (retrieved 2026-11-15)
- Page: https://planetarynames.wr.usgs.gov/GIS_Downloads
- What was done to it: Only the names the IAU has adopted are taken, each with its descriptor term, its centre (planetocentric latitude and east longitude), its diameter and its origin as the Gazetteer gives them; longitudes from 0 to 360 east are written from -180 to 180, positions to the Gazetteer's four decimals of a degree and diameters to ten metres. The features are put in order of rank: the large regions (oceani, maria, terrae, planitiae, regiones and the like) first, then the other named landforms, then the satellite features and the places named at landing sites, each by diameter. Where a satellite feature's origin is its parent's word for word, it is written once, with the parent. A feature the file lists twice under one number, with two outlines a few kilometres apart, is taken as first listed.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `gazetteer_vesta`

## GeoNames cities15000: every city of 15,000 people or more

- Publisher: GeoNames
- Licence: CC BY 4.0
- Terms: https://www.geonames.org/about.html
- Credit: GeoNames, CC BY 4.0, https://www.geonames.org/
- Page: https://download.geonames.org/export/dump/
- What was done to it: The cities the app bundles for finding a place (places/cities.tsv); on the Earth's globe the 3,000 most populous, each named as GeoNames gives it in Latin script.
- Retrieved: 2026-11-13
- Identifier in the app's lock: `geonames_cities15000`

## hyg

- Licence: CC BY-SA 4.0
- Retrieved: 2026-11-13
- Identifier in the app's lock: `hyg`

## Io Galileo SSI / Voyager Color Merged Global Mosaic 1km

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://astrogeology.usgs.gov/search/map/io_galileo_ssi_voyager_color_merged_global_mosaic_1km
- Credit: USGS Astrogeology Science Center; NASA/JPL Galileo SSI and Voyager images from the Planetary Data System
- Page: https://astrogeology.usgs.gov/search/map/io_galileo_ssi_voyager_color_merged_global_mosaic_1km
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Its colour is Galileo's violet, green and near-infrared (756 nm) images shown as blue, green and red, laid on Voyager's and Galileo's sharper monochrome mosaic, as the USGS made it: false colour, stronger than the eye would see, which the app says. Its longitudes, published west-positive, are made east-positive.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `io_galileo_voyager_colour`

## Planetary Satellite Physical Parameters

- Publisher: NASA/JPL Solar System Dynamics group
- Licence: Public domain
- Terms: https://ssd.jpl.nasa.gov/faq.html
- Credit: NASA/JPL Solar System Dynamics, Planetary Satellite Physical Parameters, data retrieved 2026-11-14
- Page: https://ssd.jpl.nasa.gov/sats/phys_par/
- What was done to it: Only the GM, mean radius and mean density of the moons named are taken, in SI units (g/cm^3 as kg/m^3). Their surface gravity and escape velocity are worked out from that GM and mean radius (GM / r^2, the square root of 2 GM / r), as JPL works the density out from them.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `jpl_satellite_physical`

## JPL Small-Body Database: 1 Ceres, its physical parameters and orbit

- Publisher: NASA/JPL Solar System Dynamics group
- Licence: Public domain
- Terms: https://ssd.jpl.nasa.gov/faq.html
- Credit: NASA/JPL Solar System Dynamics, Small-Body Database (1 Ceres), data retrieved 2026-11-14
- Page: https://ssd.jpl.nasa.gov/tools/sbdb_lookup.html#/?sstr=1
- What was done to it: Only the values named are taken, in SI units (g/cm^3 as kg/m^3, au as km with the IAU's au of 149,597,870.7 km); the mean radius is half the diameter given. Its surface gravity and escape velocity are worked out from its GM and that radius (GM / r^2, the square root of 2 GM / r), as this source gives neither. Its osculating orbit (epoch, a, e, i, node, perihelion, mean anomaly) is written by build_orientations.py into core:astronomy, which follows that ellipse to place the body in the 3D view.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `jpl_sbdb_ceres`

## JPL Small-Body Database: 4 Vesta, its physical parameters and orbit

- Publisher: NASA/JPL Solar System Dynamics group
- Licence: Public domain
- Terms: https://ssd.jpl.nasa.gov/faq.html
- Credit: NASA/JPL Solar System Dynamics, Small-Body Database (4 Vesta), data retrieved 2026-11-14
- Page: https://ssd.jpl.nasa.gov/tools/sbdb_lookup.html#/?sstr=4
- What was done to it: Only the values named are taken, in SI units (g/cm^3 as kg/m^3, au as km with the IAU's au of 149,597,870.7 km); the mean radius is half the diameter given. Its surface gravity and escape velocity are worked out from its GM and that radius (GM / r^2, the square root of 2 GM / r), as this source gives neither. Its osculating orbit (epoch, a, e, i, node, perihelion, mean anomaly) is written by build_orientations.py into core:astronomy, which follows that ellipse to place the body in the 3D view.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `jpl_sbdb_vesta`

## Hubble OPAL global map of Jupiter, 11 December 2025, colour from 395, 502 and 631 nm

- Publisher: Space Telescope Science Institute (MAST), OPAL team
- Licence: CC BY 4.0
- Terms: https://archive.stsci.edu/hlsp/opal
- Credit: NASA/ESA Hubble Space Telescope, OPAL program (PI: A. Simon), archived by STScI, doi:10.17909/T9G593
- Page: https://archive.stsci.edu/hlsp/opal/opal-jupiter-cycle-32
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Latitudes the map does not cover are left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `jupiter_opal_2025`

## Mars MGS MOLA DEM 463m

- Publisher: USGS Astrogeology Science Center
- Licence: CC0 (public domain)
- Terms: https://astrogeology.usgs.gov/search/map/mars_mgs_mola_dem_463m
- Credit: MOLA Science Team (NASA Goddard Space Flight Center); USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/mars_mgs_mola_dem_463m
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC. The rims of its craters are traced from its heights as well (tools/bodies/rims.py): each is kept as a ring of points, the outline drawn when the crater is picked out on the globe; a crater whose rim the heights do not show keeps the circle of the diameter the Gazetteer states.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `mars_mola_elevation`

## Mars Viking Global Color Mosaic 925m

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://astrogeology.usgs.gov/search/map/mars_viking_global_color_mosaic_925m
- Credit: USGS Astrogeology Science Center; NASA Viking Orbiter images from the Planetary Data System
- Page: https://astrogeology.usgs.gov/search/map/mars_viking_global_color_mosaic_925m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Its colour is from the Viking Orbiters' red and violet filters, with green made by the USGS from their average.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `mars_viking_colour`

## Mercury MESSENGER MDIS Global Color Mosaic 665m, version 3: its 750 nm band

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/mercury_messenger_mdis_global_color_mosaic_665m
- Credit: MESSENGER Team and Arizona State University, MDIS global colour mosaic; NASA/Johns Hopkins University Applied Physics Laboratory/Carnegie Institution of Washington; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/mercury_messenger_mdis_global_color_mosaic_665m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Only the mosaic's 750 nm band is used, as brightness without colour: its other two bands are at 430 and 1000 nm, which would make colours the eye does not see.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `mercury_mdis_colour`

## Mercury MESSENGER Global DEM 665m, version 2

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/mercury_messenger_global_dem_665m
- Credit: USGS Astrogeology Science Center: K. J. Becker et al. (2016), First global digital elevation model of Mercury, LPSC 47, 2959; NASA/Arizona State University/Johns Hopkins APL/Carnegie Institution for Science
- Page: https://astrogeology.usgs.gov/search/map/mercury_messenger_global_dem_665m
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC. The rims of its craters are traced from its heights as well (tools/bodies/rims.py): each is kept as a ring of points, the outline drawn when the crater is picked out on the globe; a crater whose rim the heights do not show keeps the circle of the diameter the Gazetteer states.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `mercury_mdis_elevation`

## milky_way

- Licence: Public domain (NASA/Goddard Space Flight Center Scientific Visualization Studio)
- Retrieved: 2026-11-13
- Identifier in the app's lock: `milky_way`

## CGI Moon Kit: LOLA elevation, 16 pixels a degree

- Publisher: NASA's Scientific Visualization Studio
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NASA's Scientific Visualization Studio; elevation from the LRO Lunar Orbiter Laser Altimeter team
- Page: https://svs.gsfc.nasa.gov/4720
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `moon_lola_elevation`

## CGI Moon Kit: LOLA elevation, 64 pixels a degree (the Moon's fetched tiers)

- Publisher: NASA's Scientific Visualization Studio
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NASA's Scientific Visualization Studio; elevation from the LRO Lunar Orbiter Laser Altimeter team
- Page: https://svs.gsfc.nasa.gov/4720
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC. The same model as the bundled relief's at four times its resolution, for the finer tiers fetched.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `moon_lola_elevation_64`

## CGI Moon Kit: LOLA elevation, 64 pixels a degree, in half-metres

- Publisher: NASA's Scientific Visualization Studio
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NASA's Scientific Visualization Studio; elevation from the LRO Lunar Orbiter Laser Altimeter team
- Page: https://svs.gsfc.nasa.gov/4720
- What was done to it: Not drawn as a map. The rims of its craters are traced from its heights as well (tools/bodies/rims.py): each is kept as a ring of points, the outline drawn when the crater is picked out on the globe; a crater whose rim the heights do not show keeps the circle of the diameter the Gazetteer states.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `moon_lola_elevation_64_uint`

## CGI Moon Kit: LROC colour map, 2025 version, 4096 × 2048

- Publisher: NASA's Scientific Visualization Studio
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NASA's Scientific Visualization Studio
- Page: https://svs.gsfc.nasa.gov/4720
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). NASA says of the map that it is “optimized for aesthetics, not science”: colour from the LROC WAC mosaic at 643, 566 and 415 nm, adjusted towards human vision, with the latitudes beyond 70° filled from a lower-resolution albedo map.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `moon_lroc_colour`

## CGI Moon Kit: LROC colour map, 2025 version, 8192 × 4096 (the Moon's fetched tiers)

- Publisher: NASA's Scientific Visualization Studio
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NASA's Scientific Visualization Studio
- Page: https://svs.gsfc.nasa.gov/4720
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). The same map as the bundled one at twice its size, for the finer tiers fetched (ASTC for colour on devices that read it). NASA says of the map that it is “optimized for aesthetics, not science”: colour from the LROC WAC mosaic at 643, 566 and 415 nm, adjusted towards human vision, with the latitudes beyond 70° filled from a lower-resolution albedo map.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `moon_lroc_colour_8k`

## LROC Global Mapping of Lunar Mare Boundaries, 65° N to 65° S

- Publisher: LROC Science Operations Center, Arizona State University; NASA Planetary Data System
- Licence: Public domain
- Terms: https://lroc.im-ldi.com/about/terms
- Credit: NASA/GSFC/Arizona State University: D. M. Nelson et al. (2014), Mapping lunar maria extents and lobate scarps using LROC image products, LPSC 45, 2861
- Page: https://data.lroc.im-ldi.com/lroc/view_rdr/SHAPEFILE_LROC_GLOBAL_MARE
- What was done to it: The maria's boundaries (tools/bodies/maria.py): each polygon given the name of the Gazetteer's mare, oceanus, lacus, sinus or palus whose centre it holds, or, holding none, the name its record gives where that is one of the Gazetteer's; a polygon holding several centres divided between them by the least distance from each centre over its stated radius. Every ring simplified on the sphere to within 0.088 degrees, half a texel of the Moon's bundled map, those under 120 km² left out. Kept as the outline drawn when a mare is picked out on the globe; a name the map gives nothing keeps the circle of its stated diameter.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `moon_lroc_mare`

## SLDEM2015: the Moon's elevation from LOLA and SELENE's Terrain Camera, 128 pixels a degree, 60° S to 60° N

- Publisher: NASA Planetary Data System, Geosciences Node; LRO LOLA team, NASA Goddard Space Flight Center
- Licence: Public domain
- Terms: https://pds-geosciences.wustl.edu/faq.html
- Credit: M. K. Barker et al. (2016), A new lunar digital elevation model from the Lunar Orbiter Laser Altimeter and SELENE Terrain Camera, Icarus 273, 346–355; LRO LOLA team and JAXA's SELENE team; NASA Planetary Data System
- Page: https://pds-geosciences.wustl.edu/lro/lro-l-lola-3-rdr-v1/lrolol_1xxx/data/sldem2015/
- What was done to it: Not drawn as a map. The rims of its craters are traced from its heights as well (tools/bodies/rims.py): each is kept as a ring of points, the outline drawn when the crater is picked out on the globe; a crater whose rim the heights do not show keeps the circle of the diameter the Gazetteer states.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `moon_sldem2015_128`

## pck00011.tpc: the IAU's rotation and shape of the Sun, the planets, their moons and some asteroids

- Publisher: NASA's Navigation and Ancillary Information Facility (NAIF), JPL
- Licence: Free to use (NAIF's rules)
- Terms: https://naif.jpl.nasa.gov/naif/rules.html
- Credit: IAU Working Group on Cartographic Coordinates and Rotational Elements, 2015 report (B. A. Archinal et al. 2018), as NAIF's pck00011.tpc gives it (N. Bachman, NAIF/JPL)
- Page: https://naif.jpl.nasa.gov/naif/data_generic.html
- What was done to it: Only the radii of the bodies named are taken (their two equatorial radii and their polar one), and how ten of them turn (Io, Europa, Ganymede, Callisto, Enceladus, Titan, Triton, Charon, Ceres and Vesta: their poles, prime meridians and the periodic terms of their planets' systems), which build_orientations.py writes out as a table core:astronomy turns them by; the kernel itself is not copied.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `naif_pck00011`

## Hubble OPAL global map of Neptune, 24 August 2025, colour from 467, 547 and 657 nm

- Publisher: Space Telescope Science Institute (MAST), OPAL team
- Licence: CC BY 4.0
- Terms: https://archive.stsci.edu/hlsp/opal
- Credit: NASA/ESA Hubble Space Telescope, OPAL program (PI: A. Simon), archived by STScI, doi:10.17909/T9G593
- Page: https://archive.stsci.edu/hlsp/opal/opal-neptune-cycle-32
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Latitudes the map does not cover are left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `neptune_opal_2025`

## Asteroid Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/asteroidfact.html
- What was done to it: Only the masses of Ceres and Vesta are taken, as the page gives them (in 10^15 kg, written out as kg). The page says most of its masses are rough estimates; those of Ceres and Vesta were measured by the Dawn spacecraft.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_asteroids`

## Earth Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/earthfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_earth`

## Jovian Satellite Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/joviansatfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_jovian_satellites`

## Jupiter Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/jupiterfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_jupiter`

## Mars Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/marsfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_mars`

## Mercury Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/mercuryfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_mercury`

## Moon Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/moonfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_moon`

## Neptune Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/neptunefact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_neptune`

## Neptunian Satellite Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/neptuniansatfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_neptunian_satellites`

## Pluto Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/plutofact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_pluto`

## Saturn Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/saturnfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_saturn`

## Saturnian Satellite Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/saturniansatfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_saturnian_satellites`

## Sun Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/sunfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_sun`

## Uranus Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/uranusfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_uranus`

## Venus Fact Sheet

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: the Planetary Fact Sheets, by D. R. Williams
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/venusfact.html
- What was done to it: Only the values named are taken, as the page gives them, in SI units (10^24 kg written out as kg, 10^6 km as km); nothing is rounded.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `nssdca_venus`

## openngc_addendum

- Licence: CC BY-SA 4.0
- Retrieved: 2026-11-13
- Identifier in the app's lock: `openngc_addendum`

## openngc_ngc

- Licence: CC BY-SA 4.0
- Retrieved: 2026-11-13
- Identifier in the app's lock: `openngc_ngc`

## Pluto New Horizons LORRI - MVIC Global Mosaic 300m (July 2017)

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/pluto_new_horizons_lorri_mvic_global_mosaic_300m
- Credit: New Horizons Team: NASA/Johns Hopkins University Applied Physics Laboratory/Southwest Research Institute/Lunar and Planetary Institute; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/pluto_new_horizons_lorri_mvic_global_mosaic_300m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. What New Horizons did not see is left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `pluto_nh_mosaic`

## Hubble OPAL global map of Saturn, 22 October 2023, colour from 395, 502 and 631 nm

- Publisher: Space Telescope Science Institute (MAST), OPAL team
- Licence: CC BY 4.0
- Terms: https://archive.stsci.edu/hlsp/opal
- Credit: NASA/ESA Hubble Space Telescope, OPAL program (PI: A. Simon), archived by STScI, doi:10.17909/T9G593
- Page: https://archive.stsci.edu/hlsp/opal/opal-saturn-cycle-30
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Only the north beyond about 75° N is taken from it, which Saturn's tilt hid from Hubble on 29 August 2025: its colours matched, channel by channel, to the 2025 map's at 74° to 75° N, and blended into it over a degree there. The day is said with the map.
- Retrieved: 2026-11-16
- Identifier in the app's lock: `saturn_opal_2023`

## Hubble OPAL global map of Saturn, 22 August 2024, colour from 395, 502 and 631 nm

- Publisher: Space Telescope Science Institute (MAST), OPAL team
- Licence: CC BY 4.0
- Terms: https://archive.stsci.edu/hlsp/opal
- Credit: NASA/ESA Hubble Space Telescope, OPAL program (PI: A. Simon), archived by STScI, doi:10.17909/T9G593
- Page: https://archive.stsci.edu/hlsp/opal/opal-saturn-cycle-31
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Only the band from the equator to about 5° N is taken from it, which Saturn's rings hid from Hubble on 29 August 2025: its colours matched, channel by channel, to the 2025 map's where the two meet, and blended into it over a degree at its northern edge. Saturn's bands change little from year to year; the day is said with the map.
- Retrieved: 2026-11-16
- Identifier in the app's lock: `saturn_opal_2024`

## Hubble OPAL global map of Saturn, 29 August 2025, colour from 395, 502 and 631 nm

- Publisher: Space Telescope Science Institute (MAST), OPAL team
- Licence: CC BY 4.0
- Terms: https://archive.stsci.edu/hlsp/opal
- Credit: NASA/ESA Hubble Space Telescope, OPAL program (PI: A. Simon), archived by STScI, doi:10.17909/T9G593
- Page: https://archive.stsci.edu/hlsp/opal/opal-saturn-cycle-32
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Where it has nothing, Hubble's maps of earlier years fill it, their colours matched to this map's where they meet (tools/bodies/fills.py): the band from the equator to about 5° N, which the rings hid in 2025, from the map of 22 August 2024, and the north beyond about 75° N, which the planet's tilt hid, from that of 22 October 2023. What none of them saw, round the south pole, is left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `saturn_opal_2025`

## Cassini radio occultation of Saturn's rings, 3 May 2005 (Rev 7, egress, X band from DSN 43): their normal optical depth at 10 km resolution

- Publisher: Cassini Radio Science Team (E. A. Marouf); PDS Ring-Moon Systems Node, NASA Planetary Data System
- Licence: Measurements; no terms stated; cite the data set
- Terms: https://pds.nasa.gov/home/about/
- Credit: Marouf, E., Cassini Orbiter Saturn RSS Ring Radio Occultations 2.0, CO-SR-RSS-4/5-OCC-V2.0, NASA Planetary Data System, 2018
- Page: https://pds-rings.seti.org/holdings/volumes/CORSS_8xxx/CORSS_8001/
- What was done to it: Not a picture: the normal optical depth the profile gives at each radius from 72,770 to 144,988 km (its radius with both of its corrections, for Saturn's pole and the timing), averaged over each texel of the radial strip build_rings.py makes. Where the signal was lost, the depth above the profile's threshold, it is drawn at the threshold, the least it can be (in the B ring's core, still nearly opaque). Radio light of 3.6 cm hardly sees particles much smaller than itself, so the rings are drawn as opaque as large particles make them. Inside 72,770 km (the D ring and the C ring's inner edge) the PDS table's depths are kept.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `saturn_rings_cassini_rss`

## Saturnian Rings Fact Sheet: the albedo of each ring

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: Saturnian Rings Fact Sheet (D. R. Williams)
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/satringfact.html
- What was done to it: Only the rings' albedos are taken, the middle of each range given (C ring 0.2, B and A rings 0.5, Cassini Division 0.3, F ring 0.6), as how bright the particles of each ring are in the radial strip build_rings.py makes. The rings are drawn without colour: neither page gives one.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `saturn_rings_nssdca`

## Vital Statistics for Saturn's Rings and Inner Satellites: where each ring and gap begins and ends, and its optical depth

- Publisher: PDS Ring-Moon Systems Node (SETI Institute), NASA Planetary Data System
- Licence: Measurements; no terms stated
- Terms: https://pds.nasa.gov/home/about/
- Credit: PDS Ring-Moon Systems Node, Vital Statistics for Saturn's Rings, after Murray and Dermott (1999), Colwell et al. (2009), Nicholson et al. (2014) and French et al. (2016)
- Page: https://pds-rings.seti.org/saturn/saturn_tables.html
- What was done to it: Not a picture: the rings' optical depth from their inner edge out, worked into a radial strip of 512 texels from 66,500 to 141,000 km (build_rings.py). A depth given as a range takes the geometric mean of its ends, or the middle where it starts at 0, and the B ring's region B3 its stated median, 3.6; within a ring the depth is that one value, so the strip shows where the rings and gaps are and how opaque each is, not the fine structure within them.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `saturn_rings_pds`

## stellarium_art_And

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_And`

## stellarium_art_Ant

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Ant`

## stellarium_art_Aps

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Aps`

## stellarium_art_Aql

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Aql`

## stellarium_art_Aqr

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Aqr`

## stellarium_art_Ara

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Ara`

## stellarium_art_Ari

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Ari`

## stellarium_art_Aur

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Aur`

## stellarium_art_Boo

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Boo`

## stellarium_art_CMa

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_CMa`

## stellarium_art_CMi

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_CMi`

## stellarium_art_CVn

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_CVn`

## stellarium_art_Cae

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cae`

## stellarium_art_Cam

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cam`

## stellarium_art_Cap

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cap`

## stellarium_art_Car

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Car`

## stellarium_art_Cas

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cas`

## stellarium_art_Cen

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cen`

## stellarium_art_Cep

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cep`

## stellarium_art_Cet

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cet`

## stellarium_art_Cha

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cha`

## stellarium_art_Cir

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cir`

## stellarium_art_Cnc

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cnc`

## stellarium_art_Col

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Col`

## stellarium_art_Com

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Com`

## stellarium_art_CrA

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_CrA`

## stellarium_art_CrB

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_CrB`

## stellarium_art_Crt

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Crt`

## stellarium_art_Cru

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cru`

## stellarium_art_Crv

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Crv`

## stellarium_art_Cyg

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Cyg`

## stellarium_art_Del

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Del`

## stellarium_art_Dor

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Dor`

## stellarium_art_Dra

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Dra`

## stellarium_art_Equ

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Equ`

## stellarium_art_Eri

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Eri`

## stellarium_art_For

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_For`

## stellarium_art_Gem

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Gem`

## stellarium_art_Gru

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Gru`

## stellarium_art_Her

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Her`

## stellarium_art_Hor

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Hor`

## stellarium_art_Hya

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Hya`

## stellarium_art_Hyi

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Hyi`

## stellarium_art_Ind

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Ind`

## stellarium_art_LMi

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_LMi`

## stellarium_art_Lac

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Lac`

## stellarium_art_Leo

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Leo`

## stellarium_art_Lep

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Lep`

## stellarium_art_Lib

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Lib`

## stellarium_art_Lup

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Lup`

## stellarium_art_Lyn

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Lyn`

## stellarium_art_Lyr

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Lyr`

## stellarium_art_Men

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Men`

## stellarium_art_Mic

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Mic`

## stellarium_art_Mon

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Mon`

## stellarium_art_Mus

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Mus`

## stellarium_art_Nor

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Nor`

## stellarium_art_Oct

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Oct`

## stellarium_art_Oph

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Oph`

## stellarium_art_Ori

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Ori`

## stellarium_art_Pav

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Pav`

## stellarium_art_Peg

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Peg`

## stellarium_art_Per

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Per`

## stellarium_art_Phe

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Phe`

## stellarium_art_Pic

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Pic`

## stellarium_art_PsA

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_PsA`

## stellarium_art_Psc

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Psc`

## stellarium_art_Pyx

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Pyx`

## stellarium_art_Ret

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Ret`

## stellarium_art_Scl

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Scl`

## stellarium_art_Sco

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Sco`

## stellarium_art_Sct

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Sct`

## stellarium_art_Sex

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Sex`

## stellarium_art_Sge

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Sge`

## stellarium_art_Sgr

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Sgr`

## stellarium_art_Tau

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Tau`

## stellarium_art_Tel

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Tel`

## stellarium_art_TrA

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_TrA`

## stellarium_art_Tri

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Tri`

## stellarium_art_Tuc

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Tuc`

## stellarium_art_UMa

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_UMa`

## stellarium_art_UMi

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_UMi`

## stellarium_art_Vir

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Vir`

## stellarium_art_Vol

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Vol`

## stellarium_art_Vul

- Licence: Free Art License
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_art_Vul`

## stellarium_modern

- Licence: CC BY-SA 4.0
- Retrieved: 2026-11-13
- Identifier in the app's lock: `stellarium_modern`

## Titan Cassini ISS Global Mosaic 4005m (June 2015, through flyby T100)

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/titan_cassini_iss_global_mosaic_4005m
- Credit: Cassini ISS Team: NASA/JPL-Caltech/Space Science Institute; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/titan_cassini_iss_global_mosaic_4005m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Near-infrared at 938 nm, a window through Titan's haze, with the haze divided out by the Cassini team: not what the eye would see, which the app says. What Cassini did not map is left unpainted and marked as not seen. Its longitudes, published west-positive, are made east-positive.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `titan_cassini_iss`

## Triton Voyager 2 Global Color Mosaic 600m

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/triton_voyager_2_global_color_mosaic_600m
- Credit: Lunar and Planetary Institute (P. Schenk); NASA/JPL Voyager 2; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/triton_voyager_2_global_color_mosaic_600m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Its colour is Voyager 2's orange, violet and ultraviolet images shown as red, green and blue: false colour, which the app says. Voyager saw less than half of Triton; the rest is left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `triton_voyager_colour`

## Hubble OPAL global map of Uranus, 23 October 2025, colour from 467, 547 and 657 nm

- Publisher: Space Telescope Science Institute (MAST), OPAL team
- Licence: CC BY 4.0
- Terms: https://archive.stsci.edu/hlsp/opal
- Credit: NASA/ESA Hubble Space Telescope, OPAL program (PI: A. Simon), archived by STScI, doi:10.17909/T9G593
- Page: https://archive.stsci.edu/hlsp/opal/opal-uranus-cycle-33
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Latitudes the map does not cover are left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `uranus_opal_2025`

## Uranus Rings Fact Sheet: the albedo of each ring

- Publisher: NASA Space Science Data Coordinated Archive (NSSDCA), Goddard Space Flight Center
- Licence: NASA media guidelines
- Terms: https://www.nasa.gov/nasa-brand-center/images-and-media/
- Credit: NSSDCA, NASA Goddard Space Flight Center: Uranus Rings Fact Sheet (D. R. Williams)
- Page: https://nssdc.gsfc.nasa.gov/planetary/factsheet/uranringfact.html
- What was done to it: Only the rings' albedos are taken (0.015 for every ring but the epsilon ring, 0.018 for it), as how bright the particles of each ring are in the radial strip build_rings.py makes: as dark as charcoal. The rings are drawn without colour: neither page gives one.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `uranus_rings_nssdca`

## Vital Statistics for Uranus's Rings and Inner Satellites: where each ring lies, how wide it is, and its optical depth

- Publisher: PDS Ring-Moon Systems Node (SETI Institute), NASA Planetary Data System
- Licence: Measurements; no terms stated
- Terms: https://pds.nasa.gov/home/about/
- Credit: PDS Ring-Moon Systems Node, Vital Statistics for Uranus's Rings, after French et al. (1991), Murray and Dermott (1999) and Showalter and Lissauer (2006)
- Page: https://pds-rings.seti.org/uranus/uranus_tables.html
- What was done to it: Not a picture: the rings' optical depth from 41,000 to 52,000 km, worked into a radial strip of 512 texels (build_rings.py). Each ring is drawn as a circle at its middle radius, as wide as the middle of the widths given (the rings are ellipses and vary in width round them: the epsilon ring's distance from Uranus changes by 800 km). A depth given as a range takes the geometric mean of its ends; one given as at most or at least a value takes that value. The two faint outer rings, ten thousand times less opaque, are left out.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `uranus_rings_pds`

## Venus Magellan Global Topography 4641m, version 2

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/venus_magellan_global_topography_4641m
- Credit: Magellan Team: P. Ford, G. Pettengill, F. Liu, J. Quigley; NASA/JPL; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/venus_magellan_global_topography_4641m
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `venus_magellan_elevation`

## Venus Magellan Global C3-MDIR Mosaic 2025m: radar

- Publisher: USGS Astrogeology Science Center
- Licence: Public domain
- Terms: https://astrogeology.usgs.gov/search/map/venus_magellan_global_c3_mdir_mosaic_2025m
- Credit: NASA/JPL Magellan mission; PDS Geosciences Node; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/venus_magellan_global_c3_mdir_mosaic_2025m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). A radar image at 12.6 cm, not light: brightness is how much of the radar's signal the ground sent back. What Magellan did not map is left unpainted and marked as not seen.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `venus_magellan_radar`

## Vesta Dawn FC HAMO Global DTM 93m (Claudia Double Prime longitudes)

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/vesta_dawn_fc_hamo_global_dtm_93m
- Credit: NASA/JPL-Caltech/UCLA/MPS/DLR/IDA, Dawn Framing Camera, DTM by DLR; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/vesta_dawn_fc_hamo_global_dtm_93m
- What was done to it: Turned into the app's layout and resampled onto a cube in the body's own axes; at every mip level the terrain's slopes are worked out from the heights at that level's spacing and stored as the surface normal's two components (docs/data/formats.md, "Relief maps"), compressed as EAC. Its values, Vesta's radius at each point, are taken as its shape, and the slopes stored are those against the ellipsoid the app draws Vesta as. The rims of its craters are traced from its heights as well (tools/bodies/rims.py): each is kept as a ring of points, the outline drawn when the crater is picked out on the globe; a crater whose rim the heights do not show keeps the circle of the diameter the Gazetteer states.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `vesta_dawn_dtm`

## Vesta Dawn FC HAMO Global Mosaic 60m (Claudia Double Prime longitudes)

- Publisher: USGS Astrogeology Science Center
- Licence: Free to use; please cite the authors
- Terms: https://astrogeology.usgs.gov/search/map/vesta_dawn_fc_hamo_global_mosaic_60m
- Credit: NASA/JPL-Caltech/UCLA/MPS/DLR/IDA, Dawn Framing Camera, mosaic by DLR; USGS Astrogeology Science Center
- Page: https://astrogeology.usgs.gov/search/map/vesta_dawn_fc_hamo_global_mosaic_60m
- What was done to it: Turned into the app's layout (north up, planetocentric latitude, east longitude), resampled onto the six faces of a cube in the body's own axes with every mip level made from the map itself, and compressed for the GPU (ETC2 for colour, EAC for relief). Brightness without colour. What Dawn did not see, the north in its winter, is left unpainted and marked as not seen. Its shape is drawn as the IAU's ellipsoid; its relief map carries the rest.
- Retrieved: 2026-11-14
- Identifier in the app's lock: `vesta_dawn_fc`

## Wikidata: the articles of Wikipedia about the features of the Gazetteer of Planetary Nomenclature (items with property P2824), in the editions of the app's languages

- Publisher: Wikidata, Wikimedia Foundation
- Licence: CC0 1.0
- Terms: https://www.wikidata.org/wiki/Wikidata:Licensing
- Credit: Wikidata (CC0), queried 2026-11-15
- Page: https://www.wikidata.org/wiki/Property:P2824
- What was done to it: Only which article each feature has, by the Gazetteer's number for it, is taken: the article's title in each edition that has one. An English title that does not begin with the feature's name is left out, as it may be about something else. The articles themselves are fetched from Wikipedia when they are read, under its own licence (CC BY-SA 4.0), which the app credits where it shows them.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikidata_gazetteer_articles`

## Exynos (Wikipedia, revision 1384466860)

- Publisher: Wikipedia contributors
- Licence: CC BY-SA 4.0
- Terms: https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License
- Credit: Wikipedia contributors
- Page: https://en.wikipedia.org/w/index.php?title=Exynos&oldid=1384466860
- What was done to it: Not copied: the names, part numbers, GPUs and years of the chips listed, read from the page at this revision and written into the app's table of devices (bodies/quality.json), each chip given the 3D view's tier for its GPU's generation.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikipedia_exynos`

## HiSilicon (Wikipedia, revision 1385615819)

- Publisher: Wikipedia contributors
- Licence: CC BY-SA 4.0
- Terms: https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License
- Credit: Wikipedia contributors
- Page: https://en.wikipedia.org/w/index.php?title=HiSilicon&oldid=1385615819
- What was done to it: Not copied: the names, part numbers, GPUs and years of the chips listed, read from the page at this revision and written into the app's table of devices (bodies/quality.json), each chip given the 3D view's tier for its GPU's generation.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikipedia_hisilicon`

## List of MediaTek systems on chips (Wikipedia, revision 1383869787)

- Publisher: Wikipedia contributors
- Licence: CC BY-SA 4.0
- Terms: https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License
- Credit: Wikipedia contributors
- Page: https://en.wikipedia.org/w/index.php?title=List_of_MediaTek_systems_on_chips&oldid=1383869787
- What was done to it: Not copied: the names, part numbers, GPUs and years of the chips listed, read from the page at this revision and written into the app's table of devices (bodies/quality.json), each chip given the 3D view's tier for its GPU's generation.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikipedia_mediatek`

## List of Qualcomm Snapdragon systems on chips (Wikipedia, revision 1385592133)

- Publisher: Wikipedia contributors
- Licence: CC BY-SA 4.0
- Terms: https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License
- Credit: Wikipedia contributors
- Page: https://en.wikipedia.org/w/index.php?title=List_of_Qualcomm_Snapdragon_systems_on_chips&oldid=1385592133
- What was done to it: Not copied: the names, part numbers, GPUs and years of the chips listed, read from the page at this revision and written into the app's table of devices (bodies/quality.json), each chip given the 3D view's tier for its GPU's generation.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikipedia_snapdragon`

## Google Tensor (Wikipedia, revision 1382464343)

- Publisher: Wikipedia contributors
- Licence: CC BY-SA 4.0
- Terms: https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License
- Credit: Wikipedia contributors
- Page: https://en.wikipedia.org/w/index.php?title=Google_Tensor&oldid=1382464343
- What was done to it: Not copied: the names, part numbers, GPUs and years of the chips listed, read from the page at this revision and written into the app's table of devices (bodies/quality.json), each chip given the 3D view's tier for its GPU's generation.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikipedia_tensor`

## List of UNISOC systems on chips (Wikipedia, revision 1385654015)

- Publisher: Wikipedia contributors
- Licence: CC BY-SA 4.0
- Terms: https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License
- Credit: Wikipedia contributors
- Page: https://en.wikipedia.org/w/index.php?title=List_of_UNISOC_systems_on_chips&oldid=1385654015
- What was done to it: Not copied: the names, part numbers, GPUs and years of the chips listed, read from the page at this revision and written into the app's table of devices (bodies/quality.json), each chip given the 3D view's tier for its GPU's generation.
- Retrieved: 2026-11-15
- Identifier in the app's lock: `wikipedia_unisoc`
