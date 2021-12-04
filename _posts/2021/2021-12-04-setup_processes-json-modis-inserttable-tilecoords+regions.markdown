---
layout: article
title: modis-inserttable-tilecoords+regions_v090.json
categories: setup_processes
excerpt:  Insert the MODIS db table data for tilecoords and regions from exported csv
tags:: 
    - json/modis-inserttable-tilecoords+regions
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis inserttable tilecoords+regions (setup_processes)

###  Insert the MODIS db table data for tilecoords and regions from exported csv

The json command file <span class='file'>modis-inserttable-tilecoords+regions_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "InsertTableCsv",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "tilecoords"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "InsertTableCsv",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "regions"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
