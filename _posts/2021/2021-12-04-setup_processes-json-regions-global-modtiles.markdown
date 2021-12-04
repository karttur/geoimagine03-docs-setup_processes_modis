---
layout: article
title: regions-global-modtiles_v090.json
categories: setup_processes
excerpt: \# Link global default regions to MODIS SIN grid tiles
tags:: 
    - json/regions-global-modtiles
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/regions global modtiles (setup_processes)

### \# Link global default regions to MODIS SIN grid tiles

The json command file <span class='file'>regions-global-modtiles_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "modis"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "global",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "pubroi",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "v010"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "pubroi",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "v010"
          }
        }
      ]
    }
  ]
}
```
