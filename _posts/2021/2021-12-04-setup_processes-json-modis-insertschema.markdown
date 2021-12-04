---
layout: article
title: modis-insertschema_v090.json
categories: setup_processes
excerpt:  Insert the MODIS db schema data from exported csv
tags:: 
    - json/modis-insertschema
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis insertschema (setup_processes)

###  Insert the MODIS db schema data from exported csv

The json command file <span class='file'>modis-insertschema_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "system"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "InsertSchemaCsv",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      }
    }
  ]
}
```
