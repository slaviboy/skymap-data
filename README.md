# SkyMap data

The data that SkyMap, a free astronomy app for Android, is built from and downloads: surface maps of planets and moons, the catalogue of stars and deep-sky objects, constellation art, places, the names and outlines of surface features, and every source all of it was made from; and copies of the Wikipedia articles and the Wikimedia Commons pictures the app shows, which it falls back on when Wikipedia or Commons cannot be reached.

The data lives here in public, with every source's licence and credit, so the app keeps working if a service it draws on goes away.

## Releases

Each release is a fixed set of files. Its files never change: a changed set is published as a new release (`maps-v2`, and so on).

| Release | What it holds | Size |
|---|---|---|
| [`maps-v1`](https://github.com/slaviboy/skymap-data/releases/tag/maps-v1) | The sharper maps (High and Ultra) of 16 worlds, which the app downloads on request: one archive per world, tier and GPU encoding (`moon-high-astc.7z`, `moon-high-etc2.7z`, `moon-ultra-astc.7z`, …) | 48 archives, 336 MB |
| [`maps-v2`](https://github.com/slaviboy/skymap-data/releases/tag/maps-v2) | The finer maps added after `maps-v1`: Jupiter's and Titan's High (`jupiter-high-astc.7z`, `jupiter-high-etc2.7z`, `titan-high-astc.7z`, `titan-high-etc2.7z`), and Ceres's Ultra, its colour new beside the relief `maps-v1` holds, in one archive that takes the place of `maps-v1`'s `ceres-ultra-astc.7z`. The app fetches each archive from its own release | 5 archives, 36 MB |
| [`app-data-v1`](https://github.com/slaviboy/skymap-data/releases/tag/app-data-v1) | A copy of the data inside the app: the bundled maps, surface features and outlines, the catalogue database, stars, constellation art and places | 5 archives, 20 MB |
| [`sources-v1`](https://github.com/slaviboy/skymap-data/releases/tag/sources-v1) | Every source the data above is made from, exactly as the app's tools fetched it and pinned its SHA-256: the planetary maps and elevation models of NASA, USGS and Hubble, the star and deep-sky catalogues, the gazetteer of surface features, the constellation art, the places, and the rest. One archive per source; the Moon's SLDEM2015 elevation model comes in two volumes, which `7z x moon_sldem2015_128.7z.001` joins | 178 sources in 179 archives, 6.0 GB (13 GB unpacked) |
| [`articles-v1`](https://github.com/slaviboy/skymap-data/releases/tag/articles-v1) | The openings of the Wikipedia articles about the objects in the app's catalogue, in every edition of Wikipedia the app's languages read (Chinese in its simplified and its traditional script), as Wikipedia's REST API gave them: one archive per edition, `articles-<edition>.7z`, holding one JSON of each object's title, opening, revision and link, and the picture at its head with that picture's credit. Wikipedia contributors, CC BY-SA 4.0; `ATTRIBUTION.md` links every article and the revision copied | 35,310 articles in 49 archives, 3.9 MB |
| [`pictures-v1`](https://github.com/slaviboy/skymap-data/releases/tag/pictures-v1) | The picture at the head of each of those articles, from Wikimedia Commons, at the width the app's pages show it, unchanged, with its author, licence and credit as Commons gave them: one archive for each group of the first two hex digits of the MD5 of the picture's name on Commons (`pictures-ab.7z`, as Commons files it under `…/a/ab/`), each with `pictures-ab.json`, its pictures' names, checksums and credits. Each picture keeps its own licence; `ATTRIBUTION.md` names every one | 4,578 pictures in 256 archives, 1.12 GB |
| [`app-data-v2`](https://github.com/slaviboy/skymap-data/releases/tag/app-data-v2) | The current copy of the data inside the app, made after the Solar System, the stars around us and the Milky Way were added: what `app-data-v1` holds, with the stars in three dimensions, the Milky Way model, the globular clusters, the orbits of moons and asteroids, and the manifests of this repository's releases. `app-data-v1` stays as it was | 6 archives, 22 MB |
| [`sources-v2`](https://github.com/slaviboy/skymap-data/releases/tag/sources-v2) | The sources the app's tools pinned after `sources-v1`, exactly as fetched: the Hipparcos new reduction, the globular clusters' distances, positions and Gaia members, and JPL Horizons' ephemerides of 15 moons, Ceres and Vesta from 1900 to 2100. With `sources-v1`, every source the app's tools pin. A Horizons answer is pinned by the SHA-256 of its lines but the one that says when it was made, the stamp `archives.json` gives | 21 sources in 21 archives, 133 MB |

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

The data is not under one licence. Every file keeps the licences of the sources it was made from, and [`ATTRIBUTION.md`](ATTRIBUTION.md) lists every source with its licence, terms, credit line and what was done to it. Most are public domain or CC0 (NASA, USGS, JPL). Others ask for credit (CC BY 4.0: Hubble's OPAL maps, GeoNames) or for credit and the same licence (CC BY-SA 4.0: HYG, OpenNGC, Wikipedia, whose articles' openings `articles-v1` copies). The pictures of `pictures-v1` each keep the licence Commons gives them, most public domain, CC BY or CC BY-SA, named with its author in `pictures-<group>.json` and `ATTRIBUTION.md`. Stellarium's constellation art is under the Free Art License. The Hipparcos new reduction (`sources-v2`), like the Hipparcos data within HYG, is ESA's under CC BY-NC 3.0 IGO: credit, and no commercial use. Harris's catalogue of globular clusters may be passed on only free of charge and naming its source. Anything made from a share-alike source stays under that licence.
