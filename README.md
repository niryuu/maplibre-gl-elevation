# maplibre-gl-elevation
![](https://github.com/watergis/maplibre-gl-elevation/workflows/build/badge.svg)
![](https://github.com/watergis/maplibre-gl-elevation/workflows/deploy%20gh-pages/badge.svg)
![](https://github.com/watergis/maplibre-gl-elevation/workflows/Release%20Draft/badge.svg)
![](https://github.com/watergis/maplibre-gl-elevation/workflows/Node.js%20Package/badge.svg)
![GitHub](https://img.shields.io/github/license/watergis/maplibre-gl-elevation)

This module adds elevation control to maplibre-gl.  It was forked from [mapbox-gl-elevation](https://github.com/watergis/mapbox-gl-export).

## Installation:

```bash
npm i @watergis/maplibre-gl-elevation --save
```

## Demo:

Try [codesandbox](https://codesandbox.io/s/mapbox-gl-elevation-cldfe).

See [demo](https://watergis.github.io/maplibre-gl-elevation).

![demo](./demo.gif)

## Usage:

```ts
import MaplibreElevationControl from "@watergis/maplibre-gl-elevation";
import '@watergis/maplibre-gl-elevation/css/styles.css';
import maplibregl from 'maplibre-gl';

const map = new maplibregl.Map();
map.addControl(new MaplibreElevationControl(
        'https://wasac.github.io/rw-terrain/tiles/{z}/{x}/{y}.png',
        { 
          font: ['Roboto Medium'],
          fontSize: 12,
          fontHalo: 1,
          mainColor: '#263238',
          haloColor: '#fff',
        }
    ), 'top-right');
});
```

## Development:

```bash
npm run lint # check styling of source code
npm run lint:fix # fix styling by eslint
npm run dev
```

open [http://localhost:8080](http://localhost:8080).

If there are any changes on source code, it will be reflected automatically.

## Build package:

```bash
npm run build
```

The modules will be generated under `dist` folder.

## Deploy to Github pages

```bash
npm run deploy
```

It will deploy files under `example` folder to gh-pages.

## How to release

```zsh
npm version patch # it increase patch version 0.0.X
npm version minor # it increase minor version 0.x.0
npm version major # it increase major version x.0.0
git push origin main --tag
# release CI will create draft release in Github pages, then publish it if it is ready.
# publish CI will deploy npmjs and Github Packages.
```

## Contribution

This Maplibre GL Elevation Control is still under development. so most welcome any feedbacks and pull request to this repository.
