---
layout: article
title: regions-modtiles_v090.json
categories: setup_processes
excerpt:  Link default regions to MODIS SIN grid tiles
tags:: 
    - regions-modtiles
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# regions modtiles (setup_processes)

###  Link default regions to MODIS SIN grid tiles

The json command file <span class='file'>regions-modtiles_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
  "path": null,
  "process": [
    {
      "processid": "LinkDefaultRegionsToMODIS",
      "version": "3.0",
      "parameters": {
        "dummy": null
        },
      "srcpath": {
        "volume": "geoinfo2021",
        "hdr": "shp",
        "dat": "shp"
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
      ]
    }
  ]
}
```
