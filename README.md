# SkyMap data

The data that SkyMap, a free astronomy app for Android, is built from and downloads: surface maps of planets and moons, the catalogue of stars and deep-sky objects, constellation art, places, the names and outlines of surface features, and every source all of it was made from. Copies of the Wikipedia articles and pictures the app shows are on their way.

The data lives here in public, with every source's licence and credit, so the app keeps working if a service it draws on goes away.

## Releases

Each release is a fixed set of files. Its files never change: a changed set is published as a new release (`maps-v2`, and so on).

| Release | What it holds | Size |
|---|---|---|
| [`maps-v1`](https://github.com/slaviboy/skymap-data/releases/tag/maps-v1) | The sharper maps (High and Ultra) of 16 worlds, which the app downloads on request: one archive per world, tier and GPU encoding (`moon-high-astc.7z`, `moon-high-etc2.7z`, `moon-ultra-astc.7z`, …) | 48 archives, 336 MB |
| [`app-data-v1`](https://github.com/slaviboy/skymap-data/releases/tag/app-data-v1) | A copy of the data inside the app: the bundled maps, surface features and outlines, the catalogue database, stars, constellation art and places | 5 archives, 20 MB |
| [`sources-v1`](https://github.com/slaviboy/skymap-data/releases/tag/sources-v1) | Every source the data above is made from, exactly as the app's tools fetched it and pinned its SHA-256: the planetary maps and elevation models of NASA, USGS and Hubble, the star and deep-sky catalogues, the gazetteer of surface features, the constellation art, the places, and the rest. One archive per source; the Moon's SLDEM2015 elevation model comes in two volumes, which `7z x moon_sldem2015_128.7z.001` joins | 178 sources in 179 archives, 6.0 GB (13 GB unpacked) |

On their way, made by the app's own tools:
- **`articles-v1`:** the openings of the about 33,800 Wikipedia articles the app shows, in 48 languages, one archive per language, with each article's link and licence (CC BY-SA 4.0);
- **`pictures-v1`:** the pictures on the objects' pages, each with its author, licence and credit.

Every release holds:
- **the archives:** 7z, LZMA2 with a 16 MB dictionary;
- **`archives.json`:** what each archive holds, with every file's size and SHA-256;
- **`SHA256SUMS`:** the archives' checksums;
- **`ATTRIBUTION.md`:** the sources of that release's data, each with its licence and credit line.

## Downloading and checking

```sh
base=https://github.com/slaviboy/skymap-data/releases/download/maps-v1
curl -LO "$base/moon-high-astc.7z" -LO "$base/SHA256SUMS"
sha256sum --ignore-missing -c SHA256SUMS
7z x moon-high-astc.7z
```

The app does the same: it checks an archive's SHA-256, unpacks it, and checks every file it unpacked against `archives.json` before using it.

## Licences

The data is not under one licence. Every file keeps the licences of the sources it was made from, and [`ATTRIBUTION.md`](ATTRIBUTION.md) lists every source with its licence, terms, credit line and what was done to it. Most are public domain or CC0 (NASA, USGS, JPL). Others ask for credit (CC BY 4.0: Hubble's OPAL maps, GeoNames) or for credit and the same licence (CC BY-SA 4.0: HYG, OpenNGC, Wikipedia). Stellarium's constellation art is under the Free Art License. Anything made from a share-alike source stays under that licence.
